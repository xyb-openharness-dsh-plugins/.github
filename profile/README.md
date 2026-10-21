<!--
  Organization profile homepage for github.com/xyb-openharness-dsh-plugins
  Rendered automatically by GitHub from profile/README.md in the .github repo.
-->

<p align="center">
  <img src="https://img.shields.io/badge/OpenSource-公益开源-blue" alt="Open Source" />
  <img src="https://img.shields.io/badge/Built%20on-DSH%20(DeepSeek%20Harness)-green" alt="Built on DSH" />
  <img src="https://img.shields.io/badge/Community-Plugin%20Ecosystem-purple" alt="Community Plugin Ecosystem" />
  <img src="https://img.shields.io/badge/License-见许可证文件-lightgrey" alt="License" />
</p>

<h1 align="center">
  🔥 <a href="https://info.xiao-x-bao.com.cn">小X宝社区</a> 携手
  <a href="https://github.com/anywhere-labs">Dataelement 社区</a>
</h1>

<h3 align="center">
  全心全意为肿瘤和罕见病患者的信息改善而努力！<br />
  用 AI 为肿瘤 / 罕见病 / 慢性病患者点亮希望之光 ✨
</h3>

<br /><br />

<p align="center">
  <b>天工开物旗下公益开源项目（<a href="https://www.xiaoyibao.com.cn">www.xiaoyibao.com.cn</a>）｜关注公众号【小胰宝】官方公众号，以及【小胰宝助手】-获取最新进展</b>
</p>

<br /><br />

<p align="left">
  <b>✦ 我们深知，代码不仅仅是冷冰冰的字符，更是连接开发者与患者的桥梁，是用技术守护生命的温暖力量。</b><br /><br />

  <b>◆ 2026年，作为社区重要的生态协同推动落地，我们迎来了第一位伙伴——<a href="https://github.com/anywhere-labs">Dataelement 社区</a>，依托“工作台”这一可能在 AI 应用产品化中成为 cornerstone 的产品形态，加速建立“装好就能用，自带全程病情管理体系”的全新产品。</b><br /><br />

  <b>✧ 毫无疑问，我们在未来 3 个月内，将成为 GitHub 和开源中，肿瘤与罕见病患者公益开源工具领域的一股推动力量。期待您加入，Mark the Dent，期待和开发者们一起为患者信息平权做出改变。这是一个因为参与而为千万人带来命运改变的HVT项目。</b>
</p>

<br /><br />
<h2 align="center"><b>项目宣言</b></h2>
<p align="left">

  <b>✦ 通过与 DSH-DESKTOP 的紧密协作，我们致力于为 40+ 癌症、200+ 罕见病群体打造“开箱即用、自带全程病情管理体系”的新一代 AI Agent 能力，帮助患者获得更清晰的信息、更好的决策支持与持续的随访照护。</b><br /><br />

  <b>◆ 我们相信，技术的价值不只是提高效率，而是让每一个患者都能获得更好的信息、更多的选择与更有尊严的照护体验。</b><br /><br />

  <b>✧ 因此，我们通过开放开发脚手架、插件生态扩展，诚邀开源社区中所有愿意为患者信息与福祉带来改变的开发者、研究者与伙伴，一起推动这项温暖而有意义的事业。</b>
</p>

<p align="center">
  <img src="assets/community-banner.png" alt="小X宝社区横幅" width="860" />
</p>

<p align="center">
  <a href="https://info.xiao-x-bao.com.cn">小X宝社区</a> ·
  <a href="https://www.xiaoyibao.com.cn">小胰宝官网</a> ·
  <a href="#社区仓库">社区仓库</a> ·
  <a href="#文档导航">文档</a> ·
  <a href="#贡献指南">贡献</a> ·
  <a href="#联系方式">联系我们</a>
</p>

---

## 目录

- [项目概述](#项目概述)
- [主要特性](#主要特性)
- [快速开始](#快速开始)
  - [系统要求](#系统要求)
  - [安装](#安装)
  - [基础使用示例](#基础使用示例)
- [插件生态](#插件生态)
- [社区仓库](#社区仓库)
- [患者工作台路线图](#患者工作台路线图开发目标与招募)
- [文档导航](#文档导航)
- [项目结构](#项目结构)
- [贡献指南](#贡献指南)
- [插件开发](#插件开发)
  - [最小插件示例](#最小插件示例)
  - [注册到 DSH 配置](#注册到-dsh-配置)
- [联系方式](#联系方式)
- [许可证和免责声明](#许可证和免责声明)

---

## 项目概述

**OpenHarness DSH Plugins** 是一个围绕 [DeepSeek Harness（DSH）](https://github.com/deepseek-ai/dsh) 构建的开源插件组织。DSH 是一套以 [cordis](https://github.com/cordiverse/cordis) 为核心的插件化系统，强调组合式能力与热加载。我们将其用于构建面向社区、研究与临床场景的开放型医疗 AI 插件生态。

我们以「**公益与开源**」为核心，旗舰项目 **小胰宝（XiaoYiBao）** 致力于通过 AI 提供诊疗路径支持、共享决策辅导与个性化随访建议，帮助肿瘤、罕见病与慢性病患者获得更可持续、更可理解的协同支持。

**核心目标：**

- **开放生态**：面向研究者、临床工程师与开发者开放，任何人都可以基于统一规范贡献插件。
- **安全可解释**：输出带有支持性证据与参考来源，隐私优先，避免可识别信息泄露。
- **高度可扩展**：模块化插件机制，便于接入新模型、新数据源与新场景。
- **社区驱动**：鼓励临床、研究与开发者共同参与，让技术成为连接人与希望的桥梁。

---

## 主要特性

1. **基于 DSH 的插件框架** —— 复用 DSH / cordis 的插件组合与热加载能力，插件即「可插拔的能力单元」。
2. **医疗级旗舰插件「小胰宝」** —— 面向肿瘤 / 罕见病 / 慢性病的 AI 共享决策与随访支持，已在公益场景落地。
3. **共享决策支持（DSH）** —— 以证据为导向，输出可解释的诊疗路径与决策建议，而非黑盒结论。
4. **病例结构化抽取** —— 支持从文本、影像与检查项中抽取并结构化关键病历信息。
5. **可扩展插件机制** —— 通过 `cordis.patch.yml` 的 `insert` 入口或 DSH 的插件安装入口接入第三方插件；在 DSH Desktop 内一律走 app 的工作台市场 / 已安装列表，不另起 Web 界面。
6. **多语言与本地化** —— 内置中文本地化，文档与界面支持持续扩展更多语言。

---

## 快速开始

### 系统要求

| 项目 | 要求 | 说明 |
| --- | --- | --- |
| **DSH Desktop** | 最新稳定版 | **推荐载体**。工作台与插件的安装、加载都在 app 内完成；app 自带 Node 与 pnpm，无需另装 |
| Node.js | ≥ 18（推荐 20 LTS） | **仅开发或 CLI 载体需要**，Desktop 用户不用装 |
| 包管理器 | pnpm（Desktop 自带） | 开发打包用 `pnpm pack` |
| Git | 任意较新版本 | 克隆仓库、参与贡献 |

### 安装（DSH Desktop，推荐路径）

1. 安装并启动 **DSH Desktop**，完成首次引导。
2. **设置 → 通用**，确认「启用工作台功能」处于开启状态（关掉后所有工作台都不加载，但已有会话与数据不受影响）。
3. 打开左侧 **工作台市场**，搜索病种工作台（如「小粉宝」）后安装。
4. 出现「工作台安装变更需要重启 Harness 后生效」时点 **立即重启**；没有提示时用菜单 **Harness → 重启 Harness**。
5. 回到市场切到 **已安装** 核对条目，再从左侧固定入口打开业务面板。

> ⚠️ **不要用 `dsh web` 起网页版、再到浏览器里找 Settings → Plugins 开关插件。** 那是 CLI / Web 载体，和 DSH Desktop 不是同一个 Harness、不是同一个安装位置——装上去 Desktop 侧不会加载。Desktop 的正规入口只有 app 内的工作台市场 / 已安装列表。

### 命令行安装（开发者 / 本机自测）

Desktop 自带 Harness 与 pnpm。命令行安装必须显式指向**它**的 Harness 目录，否则会装到 CLI 的 `~/.dsh`（Desktop 看不到）：

```bash
# macOS：Desktop 的 Harness 目录（其他平台以 app「关于 / 诊断」显示为准）
export DSH_HOME="$HOME/Library/Application Support/dsh-desktop/harness"
export PATH="$DSH_HOME/.desktop-bin:$PATH"   # 用 app 自带的 pnpm / node

dsh plugin add --help                        # 语法以本机 help 为准，不猜参数
dsh plugin add ./dist/my-workbench-0.1.0.tgz
```

装完仍要回到 app 内重启 Harness，并到「已安装」核对条目。**当前版本是否提供 app 内的本地 `.tgz` 安装入口要在「工作台市场／已安装」里实地确认**，没有这个入口的版本不要硬找，直接用上面的命令行方式。

> 容易踩的三个坑：
> ① **Desktop 的 Harness 不等于 `~/.dsh`**。macOS 上默认是 `~/Library/Application Support/dsh-desktop/harness`，活动 profile 目录名还偏偏叫 `web`——名字一样，位置不同。装进 `~/.dsh/profiles/*` 的那一份，Desktop 不会加载。路径以 app「关于／诊断」显示和实际加载证据为准，不要按目录名猜。
> ② `dsh --profile web --dump-config` 出现插件层只证明配置生效，**不能**当作 UI 加载证据。
> ③ 工作台要经 Desktop 的隔离 generation 安装并在 `desktop-workbenches/market-installs.json` 留记录，客户端才认得出它的工作台身份；只手工塞 `node_modules` 不会出现在左侧入口。

### 验证是否真的装上

| 证据层 | 怎么看 | 能证明什么 |
| --- | --- | --- |
| 配置层 | `dump-config` 中有本包插件层 | 只证明 patch 生效 |
| 列表层 | app 内工作台市场切到「已安装」出现条目 | 证明包被识别、注册成功 |
| 界面层 | 左侧入口打开业务面板，核心流程可点通 | **唯一算「装机通过」的证据** |

三层缺一不可；只跑到前两层时，请写「配置已加载、UI 未验证」，不要写「装机通过」。

---

## 插件生态

本组织同时维护**官方插件**与接纳**社区插件**。下表为当前生态概览（欢迎通过 PR 补充你的插件）：

| 插件 | 类型 | 简介 | 状态 |
| --- | --- | --- | --- |
| **小胰宝 XiaoYiBao** | 官方 · 医疗 | 面向肿瘤 / 罕见病 / 慢性病的 AI 共享决策、病例结构化与随访支持 | 已发布 |
| 官方示例 / 模板插件 | 官方 · 脚手架 | 用于快速创建符合本组织规范的 DSH 插件 | 规划中 |
| 文档与知识处理插件 | 官方 / 社区 | 病历、文献与指南的结构化与检索增强 | 规划中 |
| 社区贡献插件 | 社区 | 由社区开发者遵循本仓库贡献指南提交，经评审后收录 | 欢迎提交 |

> 想让你的插件出现在上表？请参阅 [贡献指南](#贡献指南) 与 [插件开发](#插件开发)。

---

## 社区仓库

除本组织的 DSH 插件外，以下社区仓库承载着更完整的医疗 AI 能力与患者社区，欢迎前往了解、使用与共建：

| 仓库 | 简介 | 链接 |
| --- | --- | --- |
| **OpenCare SkillHub** | 以患者共同决策（SDM）为基础、围绕肿瘤 / 罕见病患者真实需求建设的开源医疗 SkillHub 社区，已积累 **30+** 医疗技能包：国际治疗路径、病情管理与社区支持内容 | [github.com/opencare-skillhub](https://github.com/opencare-skillhub) |
| **PancrePal（小胰宝）** | 面向胰腺癌 / 肿瘤患者的智能 RAG 平台，基于 AI Agent 构建多癌种病情管理助手与「七色卡」工具库（基因解读 / 并发症 / 营养 / 复诊准备等） | [github.com/PancrePal-xiaoyibao](https://github.com/PancrePal-xiaoyibao) |

---

## 患者工作台路线图（开发目标与招募）

我们正在为一个个具体病种建设「本机优先」的患者工作台（病程整理 · 指标追踪 · 就诊准备，隐私数据不出设备）。目标池参照 **NCCN Guidelines® 病种目录（67 个条目）** 与 **《86 个罕见病病种诊疗指南（2025 年版）》**（合计 **153 项**），聚焦让患者能自主管理、医生可快速复盘和协作。

**153 个目标不是 153 次全流程**：按 `T0 家族样板 / T1 标准 / T2 模板化 / T3 挂靠 / T4 观察池` 分级，按波次推进，每波结束留 1–2 周回流窗口把经验沉淀进脚手架。详见 [PROGRAM-PLAN.md](PROGRAM-PLAN.md)。

| 病种工作台 | 进度 | 仓库 |
| --- | --- | --- |
| 乳腺癌 · PinkyPal 小粉宝 | 🔵 开发中（v0.8.0，G1–G3 已过） | [breast-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/breast-cancer-workbench) |
| 淋巴瘤 · LymBell 小铃铛 | 🔵 开发中（v0.3.0） | [lymphoma-workbench](https://github.com/xyb-openharness-dsh-plugins/lymphoma-workbench) |
| 卵巢癌 | 🔵 开发中（v0.1.51） | [ovarian-workbench](https://github.com/xyb-openharness-dsh-plugins/ovarian-workbench) |
| 肺癌 · 小肺宝（NSCLC + SCLC 已合并） | 🔵 RC（v0.1.2-rc.16） | [lung-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/lung-cancer-workbench) |
| 胰腺癌 PDAC · 小胰宝（历史旗舰，未走脚手架） | 🔵 v0.1.29 | [xyb-workbench](https://github.com/xyb-openharness-dsh-plugins/xyb-workbench) |
| 结直肠癌 · 小畅宝（消化族样板） | 🔵 v0.1.0 开发版已推送（待 DSH 装机验证） | [colorectal-workbench](https://github.com/xyb-openharness-dsh-plugins/colorectal-workbench) |
| 胃癌 · 小胃宝 | 🔵 v0.1.0 开发版已发布（tag v0.1.0，待 DSH 装机验证） | [gastric-workbench](https://github.com/xyb-openharness-dsh-plugins/gastric-workbench) |
| 食管癌 · 小咽宝 | 🟡 v0.1.0 | [esophageal-workbench](https://github.com/xyb-openharness-dsh-plugins/esophageal-workbench) |
| 宫颈癌 · 小莲宝 | 🟡 v0.1.0 | [cervical-workbench](https://github.com/xyb-openharness-dsh-plugins/cervical-workbench) |
| 肛管癌 · AnalPal 小萌宝（2026-10-21 认领） | 🟡 v0.1.1 | [anal-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/anal-cancer-workbench) |
| 胃肠间质瘤 GIST · GistPal 小吉宝（2026-10-21 认领） | 🟡 v0.1.0 | [gist-workbench](https://github.com/xyb-openharness-dsh-plugins/gist-workbench) |
| 罕见病形态样板 · FSHD 小飞侠 | 🟡 v0.1.1 | [fshd-workbench](https://github.com/xyb-openharness-dsh-plugins/fshd-workbench) |
| 罕见病 · ATTR 淀粉宝宝（2026-10-21 认领） | 🟡 v0.1.0 | [attr-workbench](https://github.com/xyb-openharness-dsh-plugins/attr-workbench) |
| 心理支持（跨病种共用模块） | 🟢 v0.3.14 | [xiaoxinbao-workbench](https://github.com/xyb-openharness-dsh-plugins/xiaoxinbao-workbench) |
| 其余主要癌种 + 84 项罕见病 | ⬜ **招募认领中**（完整分级与招募对象见 BACKLOG） | [BACKLOG.md](BACKLOG.md) |

> 🔥 **现在最缺人的 12 个**（ATTR 已认领，其余 11 个仍在招募）：[BACKLOG §〇 优先招募榜](BACKLOG.md#〇现在最缺人优先招募榜) 按「帮扶人群规模 · 信息差 · 危重与时间压力」三维挑选，每项写明**缺什么角色**（👤 患者家属 / 🩺 临床 / 💻 开发 / 📝 内容 / 🤝 病友组织 / 👨‍👩‍👧 患儿家长）和**第一步能做什么**，并附一键认领链接。
>
> 🤝 **诚邀加入**：无论你是开发者、临床/研究者、病友组织志愿者还是写作者，都可以认领一个病种或一个模块。四种投入档位（整仓 / 模块 / 内容访谈 / 脚手架）见 **[CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md)**，从 Issue 模板开始。**不需要写代码也能贡献**——一次真实经历访谈、一份就诊问题清单都在缺。所有工作台只做信息整理，不做诊断建议。
>
> 🔒 **仓库可见性**：病种工作台一律 private（仅本组织 public 仓库与 `xyb-workbench-starter` 可公开浏览），因此上表里的病种仓库链接对组织外访客会 404，属预期。外部贡献者的协作方式：**Issue 层认领与评审不需要任何权限**，需要写代码时再由维护者逐人最小授权（见 [CONTRIBUTING §10.3](CONTRIBUTING-WORKBENCH.md)）。

---

## 文档导航

- **快速开始**：见上方 [快速开始](#快速开始)
- **插件开发指南**：见下方 [插件开发](#插件开发)
- **患者工作台路线图与病种认领**：[ROADMAP.md](ROADMAP.md)
- **规模化开发总纲**（分层分级 / 波次 / 七道质量锁）：[PROGRAM-PLAN.md](PROGRAM-PLAN.md)
- **153 项目标池分层表、招募对象与认领状态**：[BACKLOG.md](BACKLOG.md)（含 [§〇 优先招募榜](BACKLOG.md#〇现在最缺人优先招募榜)）
- **脚手架迭代与经验回流**：[SCAFFOLD-ITERATION.md](SCAFFOLD-ITERATION.md)
- **贡献手册（四条路径 / 闸口 / PR 自检）**：[CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md)
- **贡献流程**：见下方 [贡献指南](#贡献指南)
- **项目结构**：见下方 [项目结构](#项目结构)
- **小胰宝官网**：<https://www.xiaoyibao.com.cn>
- **小X宝社区**：<https://info.xiao-x-bao.com.cn>
- **OpenCare SkillHub 社区仓库**：<https://github.com/opencare-skillhub>
- **PancrePal（小胰宝）社区仓库**：<https://github.com/PancrePal-xiaoyibao>
- **DSH 官方仓库**：<https://github.com/deepseek-ai/dsh>
- **cordis 插件框架**：<https://github.com/cordiverse/cordis>

> 更完整的 Wiki / API 文档链接将随生态完善逐步补充，欢迎认领文档建设。

---

## 项目结构

本组织采用「元仓库（`.github`）+ 各插件独立仓库 / 子目录」的组织方式：

```text
xyb-openharness-dsh-plugins/
├── .github/                      # 组织元仓库（本仓库）
│   ├── profile/
│   │   └── README.md             # 组织首页（即本文件，由 GitHub 自动渲染）
│   └── README.md                 # 本仓库说明
├── plugins/                      # 官方插件源码（可为子仓库或子目录）
│   └── xiaoyibao/               # 旗舰插件：小胰宝
├── templates/                    # 插件脚手架与示例模板
├── docs/                         # 文档与规范
├── CONTRIBUTING.md               # 贡献指南
└── LICENSE                       # 许可证
```

> 注：实际目录可能随仓库调整；上述结构为推荐布局，便于新成员快速定位。

---

## 贡献指南

我们欢迎一切形式的贡献：代码、文档、翻译、Issue 反馈与插件孵化。

**患者工作台的详细贡献手册见 [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md)**，含四条贡献路径（病种认领 / 模块 / 内容与医学核对 / 脚手架）、三闸口、PR 自检清单与评审清单。

### 贡献流程

1. **认领或提出议题**：在 [Issues](https://github.com/xyb-openharness-dsh-plugins) 中搜索或新建议题，讨论需求与方案；认领病种请用「病种认领」模板，并在 Issue 下评论 `/claim` 完成领取。
2. **Fork 并创建分支**：从目标仓库的 `main` 切出特性分支，命名如 `feat/your-feature` 或 `fix/your-bug`。
3. **本地开发与自测**：遵循本组织的插件规范与代码风格，确保通过现有检查与基础测试（`npm run check`）。
4. **提交变更**：提交信息建议遵循 [Conventional Commits](https://www.conventionalcommits.org/)（如 `feat:`, `fix:`, `docs:`）。
5. **发起 Pull Request**：描述改动动机、范围与验证方式；如涉及医疗相关内容，请额外说明安全与隐私考量。
6. **评审与合入**：至少一名维护者评审通过后合入；涉及闸口或数据契约的改动需两名。

> ⚠️ **质量口径**：`npm run check` 通过只是 V1；还需 V2（Desktop profile 真加载）与 V3（真机业务闭环），**三层缺一不算通过**。**「PR 已合并」不等于「已上线/已验证」。**

### 四条不可让步

1. 不做诊断与处置建议（不写"建议治疗/可能复发/可以停药/无需就医/治愈率"）。
2. 患者数据本机优先，不引入静默上传。
3. 医学内容标注来源与版本；未核实项写「未核实」，不用相邻疾病外推。
4. 不复制指南临床内容，只引用病种名称与版本号作为范围参照。

### 行为准则

请保持友善、专业与包容。我们遵循常见的开源行为准则，禁止任何形式的骚扰或歧视性言行。

### 签署与许可

提交即表示你同意以本组织当前许可证（见 [LICENSE](LICENSE)）发布你的贡献，并确认你有权据此授权。

---

## 插件开发

DSH 插件本质上是符合 [cordis](https://github.com/cordiverse/cordis) 规范的 npm 包。下面给出一个最小可运行插件的骨架。

### 最小插件示例

`package.json`：

```json
{
  "name": "@your-scope/dsh-plugin-hello",
  "version": "0.1.0",
  "type": "module",
  "main": "lib/index.js",
  "peerDependencies": {
    "@deepseek-ai/cordis": "^4.0.1"
  }
}
```

`src/index.ts`（编译产物输出到 `lib/index.js`）：

```ts
import { Context } from '@deepseek-ai/cordis'

export const name = 'hello'
export const using = [] as const

export function apply(ctx: Context) {
  ctx.on('ready', () => {
    console.log('Hello from your DSH plugin!')
  })
}
```

### 注册到 DSH 配置

插件包被装进目标 profile 的 `node_modules` 后，由 `cordis.patch.yml` 的 `insert` 入口加载：

```yaml
# <目标 profile>/cordis.patch.yml
- insert:
    - id: hello
      name: '@your-scope/dsh-plugin-hello'
```

安装方式取决于**目标载体**（两者不通用）：

| 载体 | 安装方式 | 目标 profile（以实际加载为准） |
| --- | --- | --- |
| DSH Desktop | 工作台：左侧「工作台市场」搜索后安装，装完重启 Harness<br>本机自测：`DSH_HOME` 指向 Desktop Harness 后 `dsh plugin add` | 默认 `~/Library/Application Support/dsh-desktop/harness/profiles/web`，**不是** `~/.dsh` |
| CLI / Web | `dsh plugin add --help` 确认语法后安装 | `~/.dsh/profiles/web` |

> 工作台（workbench）**只能**装到 Desktop 那侧：除了 bundle，它还要经过 Desktop 的隔离 generation 安装流程并在 `desktop-workbenches/market-installs.json` 留记录，客户端才认得出它的工作台身份。只塞 `node_modules` 不会出现在左侧入口，也不会被市场识别为「已安装」。

开发约定：

- 插件包名建议使用 `@<scope>/dsh-plugin-<name>` 形式，便于识别与聚合。
- 仅声明必要的 `peerDependencies`（如 `@deepseek-ai/cordis` 与对应的 `@deepseek-ai/dsh-client-*`），避免与宿主重复打包。
- 涉及医疗等敏感场景时，输出需可解释、可溯源，并默认隐私优先。

---

## 联系方式

- **官方公众号**：【小胰宝】（获取最新进展与知识文章）
- **官方网站**：<https://www.xiaoyibao.com.cn> ／ 社区：<https://info.xiao-x-bao.com.cn>
- **GitHub Issues**：用于缺陷反馈与功能建议 —— [xyb-openharness-dsh-plugins](https://github.com/xyb-openharness-dsh-plugins)
- **GitHub Discussions**：用于想法交流与新插件提案（如已开启）
- **邮件**：opensource@xiaoyibao.com.cn（请以实际公布地址为准）

---

## 许可证和免责声明

### 许可证

本项目以开源许可证发布，具体条款见仓库根目录的 [LICENSE](LICENSE) 文件。插件可在此基础上附加各自条款，但须兼容本组织许可证。

### 免责声明

- **非医疗建议**：本组织提供的插件（尤其是「小胰宝」等医疗相关插件）所生成的内容**仅供研究与信息参考，不构成任何形式的专业医疗诊断、治疗建议或诊疗决策**。
- **AI 生成内容**：插件输出由人工智能模型生成，可能存在错误或偏差，使用前请自行核验关键信息与引用来源。
- **隐私优先**：使用涉及个人健康信息的功能时，请遵循所在地区的数据保护法规，避免上传可识别个人身份信息；本组织不对因误用导致的信息泄露承担责任。
- **责任限制**：在适用法律允许的最大范围内，本组织及其贡献者对使用本组织插件产生的任何直接或间接损失不承担责任。

---

<p align="center">
  用技术守护生命，用开源连接希望 —— 欢迎加入 OpenHarness DSH Plugins。
</p>
