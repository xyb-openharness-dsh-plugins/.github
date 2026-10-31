# 开发与贡献指南 · OpenHarness DSH Plugins

> 状态：组织级开发指南（v0.1，2026-10-29）。
> 面向：工作台开发者、临床/研究团队二次开发、社区志愿者、外部 API/能力提供方。
> 工作台业务贡献的详细路径见 [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md)；架构见 [ARCHITECTURE.md](ARCHITECTURE.md)。

---

## 1. 先选你的角色

| 角色 | 你可以做什么 | 从哪里开始 |
| --- | --- | --- |
| 开发者 | 新建病种工作台、补模块、修 bug、接 MinerU/OCR/知识库 | 本文 + [xyb-workbench-starter](https://github.com/xyb-openharness-dsh-plugins/xyb-workbench-starter) |
| 临床/研究团队 | 二次开发、字段与流程校对、病种差异化 | [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md) 路径 C |
| 患者/家属/志愿者 | 访谈、内容核对、就诊问题清单、试用反馈 | [BACKLOG.md](BACKLOG.md) + Issue 模板 |
| 社区运营/病友组织 | 认领病种、组织培训、帮扶使用 | [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md) 路径 A |
| API/能力提供方 | knows、RAG、OCR、心理/营养/影像/基因解读 | 本文 §6 + 组织 Issue |

许可：本组织推荐/默认 **MIT**；历史仓库以各自 `LICENSE` 为准，使用前请查看目标仓库。

---

## 2. 环境准备

| 项目 | 要求 |
| --- | --- |
| Node.js | 22+（与 DSH Desktop 基线一致） |
| 包管理器 | pnpm（DSH Desktop 自带；开发机也可单独安装） |
| DSH Desktop | 最新稳定版，用于真机安装/验收 |
| Git | 任意较新版本 |

> Desktop 的 Harness 目录不是 `~/.dsh`。macOS 默认是
> `~/Library/Application Support/dsh-desktop/harness`；活动 profile 目录名叫 `web`，但位置与 CLI 的 `~/.dsh/profiles/web` 不同。装错位置的表现是“安装成功但左侧没有入口”。

---

## 3. 仓库地图

| 仓库/目录 | 用途 |
| --- | --- |
| `xyb-workbench-starter` | 工作台脚手架、合同文档、模板 |
| `*-workbench` | 各病种工作台（多数 private；公开展示见 PROJECTS.md） |
| `.github` | 组织首页、贡献手册、路线图、Issue/PR 模板 |
| `awesome-dsh-workbench` | 工作台市场目录（收录与发布，不属于本组织代码） |
| `dsh-desktop` | 宿主（Electron + Harness），不是本组织仓库 |

一个工作台仓库的典型结构（参考 `breast-cancer-workbench`）：

```text
dsh/               服务端：store/server/import/mineru/intake/readmodels
public/            业务页面：原生单页 + 模块化 JS/CSS
schema/            SQLite 迁移（NNNN_*.sql，冻结后只增不改）
lib/               宿主客户端入口（client.js）与布局/身份常量
scripts/           构建、检查、打包
test/              单测与契约测试
docs/              设计、验收、数据合同
cordis.patch.yml   宿主插件清单
```

---

## 4. 新建一个工作台

1. 用 starter 初始化仓库（复制或按模板生成）。
2. 设置 `package.json` 的 `name/repository/version`，不要手写第二份身份常量。
3. 在 `lib/layout.js` 定义面板参数（`businessSide='left'`、`businessWidth=0.65`、`customFrame=true`、`AGENT_PANE` 25%–45%）。
4. 实现 `src/client.js` 的 `Panel`：
   - 首个子元素是语义 `<header>`，避让 `--dsh-frame-leading-clearance`；
   - 原生 `conversation` 节点始终挂载，只切 `display`；
   - splitter 可拖、可键盘调、宽度持久化；
   - 窄屏 <760px 改覆盖式抽屉。
5. 跑 `scripts/build-client.mjs` 生成 `lib/client.js`（宿主不认原生 ESM）。
6. 业务页面放 `public/`，数据层放 `dsh/`，不要在前端直连数据库。
7. 跑检查与真机安装（见 §7）。

---

## 5. 关键合同

### 5.1 面板

- `customFrame: true`；业务区在左，原生会话在右。
- 宿主校验 `businessSide` / `businessWidth`；不要传 0 或省略。
- 不复制宿主公共入口（市场、工作台切换、设置）。
- 不建第二套聊天 UI；AI 用原生会话。

### 5.2 原生会话与 AI

- `desktopWorkbenches.ensureSession({ folder })` 创建/恢复会话。
- `sessions.scope(id).get('conversation').input`：
  - `setDraft(text)` 写草稿；
  - `submit()` 发送；自动发送前必须双守卫（`phase === 'plain'` 且草稿非空）。
- 原生 `input` 不能程序化添加多文件附件；多文件先解析成文本/片段，或由用户拖进输入框。
- 只带已确认事实；未核对候选只报条数、不带值。

### 5.3 数据与候选

- 一个资料库（workspace）内多 `subject`；所有业务表带 `subject_id`。
- 原件、解析文本、候选、事实分层；删除/更正可追溯。
- 候选：`candidate`；确认后才写 `record` + `observation` / `treatment_event` + `source_ref`。
- 迁移：`schema/NNNN_*.sql`，已执行文件不改；用新文件加字段。

### 5.4 资料目录

- 不静默建目录；用户确认后才创建。
- 拒绝根目录、用户主目录、桌面根目录、系统目录。
- 路径读取做根目录边界检查。

---

## 6. 接入新能力

### 6.1 MinerU / OCR

- 统一出口：原件 → 解析文本（markdown/content_list）→ 候选。
- MinerU 需要用户同意 + Token；Token 只放 `.secrets/mineru.json` 或环境变量，不进仓库。
- 批量解析用 MinerU batch（一次多个 `data_id`），不要逐份串行。
- 失败不产候选、原件保留；401/超时/任务失败分别给可操作提示。
- 其它 OCR 以适配器接入，输出同一套 `{ text, pageRef, tables }` 结构；具体选型（DeepSeek-OCR2 / GLM-OCR / PaddleOCR-VL-1.5 / Youtu-Parsing / Indra OCR）见 [CONTRIBUTING §2.2](CONTRIBUTING.md#22-其它-ocr-工具与项目多通道)。

### 6.2 知识库

- 文件存正文：`parsed/<docId>.md`；SQLite 存 `artifact/chunk/FTS`。
- 检索返回 `document_id + page_ref + 片段 + 引用`。
- 事实库是真相层；知识库只做检索，不替代事实。
- 向量检索作为可选增强，索引必须可重建。

### 6.3 外部 API（knows / XYB RAG / 心理 / 营养 / 影像 / 基因）

- 用适配器封装：输入、输出、超时、重试、错误码、来源/时效/适用范围。
- 需要用户同意与发送范围说明；默认只发必要片段。
- 外部结果只作为候选/参考，不直接写事实库。
- 不把第三方 Key 写进仓库；用设置或 `.secrets`。

### 6.4 AI 抽取（可选）

- AI 只产 `candidate`，不写 `record`。
- 每条候选带 `sourceQuote`、`pageRef`、`confidence`、`extractor`、`modelVersion`。
- 进现有核对页，人工 accept/edit/reject；批量接受只收高置信无问题项。
- **不要让 AI 读完整 schema / 写 SQL**：只给任务合同（小 JSON Schema）或窄工具 `propose_candidates`；服务端映射到表。
- **批量不要靠一条长对话**：每份文档一个 `extraction_run`，无状态、可重试、幂等；对话只做交互。
- **AI 回复回传**：当前公开合同只有 `setDraft/submit`，没有完成事件；在宿主补 `completed` 事件前，只能做“手动导入/粘贴”，不要写“自动入库”。
- **可靠性**：`extraction_run` 需要租约/重试/取消/崩溃重领；候选幂等按来源定位（run + 日期 + pageRef/quote），不要只用 `document+field+value`；文件/DB/FTS 用状态+对账，不承诺一个原子事务。
- 详细 SQL 写入路径见 [ARCHITECTURE.md §6](ARCHITECTURE.md#6-ai-抽取结果如何写入-sqlite底层)；任务模型见 §6.5/§6.6；可靠性边界见 §2.4。

---

## 7. 本地开发与验收

```bash
# 以目标工作台仓库为准
npm ci
npm start                 # 独立开发版
npm test                  # 单测
npm run check             # 语法/schema/包合同/测试
npm run pack:check        # 包内容
npm pack                  # 生成 tgz
```

真机安装（macOS）：

```bash
export DSH_HOME="$HOME/Library/Application Support/dsh-desktop/harness"
export PATH="$DSH_HOME/.desktop-bin:$PATH"

# 用 Desktop 自带的 pnpm；版本与 profile 的 store 要匹配
npx --yes pnpm@10.15.0 --dir "$DSH_HOME/profiles/web" add -w ./your-workbench.tgz
```

装完 **重启 Harness**（或 Cmd+Q 重开 Desktop），再到工作台市场「已安装」核对条目。

### 三层验收

| 层 | 证据 | 能证明什么 |
| --- | --- | --- |
| 配置层 | `dump-config` 有插件层 | 只证明 patch 生效 |
| 列表层 | 市场「已安装」有条目 | 包被识别 |
| 界面层 | 左侧入口打开，核心流程可点通 | **唯一算装机通过** |

静态检查不能替代真机流程；涉及启动、profile、插件、目录选择、更新的改动必须走真实应用。

---

## 8. 贡献流程

1. 先看 [BACKLOG.md](BACKLOG.md) / [PROJECTS.md](PROJECTS.md)，用 Issue 模板认领病种或模块。
2. 在 Issue 里写清：目标用户、核心流程、数据来源、是否需要外部 API、隐私边界。
3. 分支开发；只改本仓库，不夹带无关文件。
4. 跑 `npm run check`；涉及 UI/安装的附真机截图/录屏。
5. PR 描述贴自检清单；维护者按 [CONTRIBUTING-WORKBENCH.md §6](CONTRIBUTING-WORKBENCH.md) 评审。
6. 合并后由维护者发版/装市场；PR 合并不等于市场立即可见。

### 四条不可让步

- 不做诊断、治疗建议、疗效判断。
- 不静默上传患者资料；外部调用必须说明发送内容。
- 未核对候选不进事实层；AI 不直接写库。
- 不把真实患者信息、API Key 写进仓库/Issue/日志/截图。

---

## 9. 安全与隐私

- 不提交 `.secrets/`、`.env`、真实 Token、数据库文件、患者资料。
- 日志/错误消息不回显 Token；只给掩码与来源。
- 外部 API 默认最小发送；用户可关闭。
- 删除/更正可追溯；导出前确认范围。

---

## 10. 常见问题

| 现象 | 原因 | 处理 |
| --- | --- | --- |
| 安装成功但左侧无入口 | 装到了 `~/.dsh` 而不是 Desktop Harness | 用 `DSH_HOME=~/Library/Application Support/dsh-desktop/harness` 重装 |
| 保存 Token 报 404 | 运行中的 Harness 是旧进程 | Cmd+Q 重开 Desktop |
| MinerU 401 | Token 过期/被环境变量覆盖 | 看设置来源；保存 `.secrets` 或清理旧 `MINERU_TOKEN` |
| 解析成功但 0 候选 | 文档不是检验单/指标不在字典 | 查看解析文本，改资料类型或人工补录 |
| 修改没生效 | 客户端 bundle 未重建/未重启 | 跑 `build-client`，重启 Harness |

---

## 11. 相关文档

- [ARCHITECTURE.md](ARCHITECTURE.md) —— 三层架构、AI/MinerU/知识库、SQLite 写入路径
- [INSTALL.md](INSTALL.md) —— 安装、验证、升级/回滚、排错
- [USAGE.md](USAGE.md) —— 适合谁、第一次使用、数据与隐私
- [CONTRIBUTING.md](CONTRIBUTING.md) —— 贡献入口与角色
- [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md) —— 工作台四条贡献路径
