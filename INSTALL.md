# 安装与验证 · OpenHarness DSH Plugins

> 状态：组织级安装说明（v0.1，2026-10-29）。
> 适用于 DSH Desktop 上的病种工作台；开发者本地打包见 [DEVELOPMENT.md](DEVELOPMENT.md)，第一次使用见 [USAGE.md](USAGE.md)。

---

## 1. 系统要求

| 项目 | 要求 | 说明 |
| --- | --- | --- |
| DSH Desktop | 最新稳定版 | **推荐载体**；工作台安装/加载都在 app 内完成 |
| 操作系统 | macOS（Apple Silicon / Intel）或 Windows x64 | 以 DSH Desktop 支持范围为准 |
| Node.js | ≥ 18（推荐 20/22） | **仅开发或 CLI 自测需要**；Desktop 用户不用装 |
| 包管理器 | pnpm（Desktop 自带） | 开发打包用 |
| Git | 任意较新版本 | 克隆仓库/参与贡献 |

许可：本组织推荐/默认 **MIT**；具体以目标仓库 `LICENSE` 为准。

---

## 2. 安装 DSH Desktop

1. 从 [dshdesktop.com](https://dshdesktop.com/zh/) 下载并安装 DSH Desktop。
2. 启动后完成首次引导。
3. **设置 → 通用** 确认「启用工作台功能」已开启（关闭后所有工作台都不加载）。

---

## 3. 从工作台市场安装（推荐）

1. 打开左侧 **工作台市场**。
2. 搜索病种工作台（如「小粉宝」「小铃铛」）。
3. 选择安装；出现「工作台安装变更需要重启 Harness 后生效」时点 **立即重启**。
4. 没有提示时，用菜单 **Harness → 重启 Harness**。
5. 回到市场切到 **已安装**，核对条目。
6. 从左侧固定入口打开业务面板。

> 不要用 `dsh web` 起网页版再找 Settings → Plugins。那是 CLI/Web 载体，和 Desktop 不是同一个 Harness、不是同一个安装位置；装上去 Desktop 不会加载。

---

## 4. 命令行安装（开发者 / 本机自测）

Desktop 自带 Harness 与 pnpm。必须显式指向 **Desktop 的 Harness 目录**：

```bash
# macOS
export DSH_HOME="$HOME/Library/Application Support/dsh-desktop/harness"
export PATH="$DSH_HOME/.desktop-bin:$PATH"

# 用 Desktop 自带 pnpm；版本要与 profile 的 store 匹配
npx --yes pnpm@10.15.0 --dir "$DSH_HOME/profiles/web" add -w ./your-workbench.tgz
```

Windows 以 app「关于 / 诊断」显示的 Harness 路径为准。

装完仍要 **重启 Harness**，再到「已安装」核对条目。

### 三个常见坑

1. **Desktop Harness ≠ `~/.dsh`**。macOS 默认是 `~/Library/Application Support/dsh-desktop/harness`；活动 profile 目录名也叫 `web`，但位置不同。装进 `~/.dsh/profiles/*` 的那份 Desktop 不加载。
2. **`dump-config` 有插件层 ≠ UI 已加载**。配置层只证明 patch 生效。
3. **手工塞 `node_modules` 不会出现在左侧入口**。工作台要经 Desktop 的安装/注册流程，客户端才认得出身份。

---

## 5. 三层验证（缺一不可）

| 层 | 怎么看 | 能证明什么 |
| --- | --- | --- |
| 配置层 | `dump-config` 中有本包插件层 | 只证明 patch 生效 |
| 列表层 | 市场「已安装」出现条目 | 包被识别、注册成功 |
| 界面层 | 左侧入口打开业务面板，核心流程可点通 | **唯一算“装机通过”** |

只到前两层时，请写「配置已加载、UI 未验证」，不要写「装机通过」。

---

## 6. 第一次使用（简版）

1. 打开工作台，点「＋ 新建档案」：填姓名、选择患者本人/家属（必填）。
2. 首屏点「一键创建默认资料目录」，或选择自己的资料目录。
3. 把病历文件放进分类目录：病理、影像、化验、出院小结、处方、康复建议、其他。
4. 点「检查我放进去的文件」→ 勾选 → 导入。
5. 点「开始解析」：文本类本机解析；扫描件/图片/PDF/Office 走 MinerU（需同意 + Token）。
6. 解析后看结果：逐份成功/失败原因；0 候选可看「解析文本」或改资料类型。
7. 「去核对」逐项接受/改后接受/拒绝；确认后才写入事实层。
8. 在「病情一图秀 / 就诊准备」查看整理结果，或导出带去沟通。

完整说明见 [USAGE.md](USAGE.md)。

---

## 7. 更新 / 卸载 / 回滚

- **更新**：市场刷新 → 安装新版本 → 按提示重启 Harness。已安装工作台仍需手动更新。
- **卸载**：市场「已安装」→ 移除 → 重启 Harness。会话、资料目录与业务数据默认保留；删除资料目录才会删除资料。
- **回滚**：保留上一个 `.tgz` 或旧版本包；用命令行 `pnpm add -w <旧包>` 重装，再重启 Harness。
- **配置备份**：安装前可备份 profile 的 `package.json` / `pnpm-lock.yaml`；出问题可恢复后重装。

---

## 8. 排错

| 现象 | 可能原因 | 处理 |
| --- | --- | --- |
| 市场里找不到 | 工作台功能关闭 / 市场未刷新 | 设置开启工作台；刷新市场 |
| 安装成功但左侧无入口 | 装错 Harness/Profile | 用 Desktop Harness 路径重装；确认「已安装」有条目 |
| 保存 Token 报 404 | 运行中的 Harness 是旧进程 | Cmd+Q 重开 Desktop，再保存 |
| MinerU 401 / Token 无效 | Token 过期，或被旧 `MINERU_TOKEN` 环境变量覆盖 | 看设置来源；保存 `.secrets` 或清理旧环境变量 |
| 解析成功但 0 候选 | 文档不是检验单 / 指标不在字典 | 看「解析文本」，改资料类型或人工补录 |
| 解析失败 | 未同意上传 / 无 Token / 网络 / OCR 质量 | 勾选同意、填 Token、重试或换原件 |
| 改了代码没生效 | 客户端 bundle 未重建/未重启 | 重建 `lib/client.js`，重启 Harness |

### 环境变量 Token 的坑

- 优先级：显式 > `.secrets/mineru.json` > `MINERU_TOKEN` > 随包公益 Key。
- 旧的环境变量会盖住新保存的 Token；现象是“换了 Token 还是 401”。
- 处理：在界面保存 `.secrets`（优先级更高），或清理 shell/启动环境里的旧 `MINERU_TOKEN`，再重启 Desktop。

---

## 9. 数据与隐私

- 资料默认只存在你选择的资料目录；工作台不在默认位置静默建目录。
- MinerU 只上传需要解析的原件；TXT/MD/CSV 始终本机抽取。
- 外部 API 调用应说明发送内容；可关闭。
- 不要把真实患者资料、Token、数据库文件提交到仓库或 Issue。
- 工作台只做信息整理，不做诊断/治疗建议。

---

## 10. 相关文档

- [ARCHITECTURE.md](ARCHITECTURE.md) —— 三层架构与数据写入
- [DEVELOPMENT.md](DEVELOPMENT.md) —— 开发、测试、打包、贡献
- [USAGE.md](USAGE.md) —— 适合谁、完整使用流程
- [CONTRIBUTING.md](CONTRIBUTING.md) —— 贡献入口
