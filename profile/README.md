<!--
  Organization profile homepage for github.com/xyb-openharness-dsh-plugins
  Rendered automatically by GitHub from profile/README.md in the .github repo.
-->

<p align="center">
  <img src="https://img.shields.io/badge/OpenSource-公益开源-blue" alt="Open Source" />
  <img src="https://img.shields.io/badge/Built%20on-DSH%20Desktop-green" alt="Built on DSH" />
  <img src="https://img.shields.io/badge/Community-Plugin%20Ecosystem-purple" alt="Community Plugin Ecosystem" />
  <img src="https://img.shields.io/badge/License-MIT%20(per%20repo)-green" alt="License" />
</p>

<h1 align="center">
  🔥 <a href="https://info.xiao-x-bao.com.cn">小X宝社区</a> 携手
  <a href="https://github.com/dataelement">Dataelem（数据项素）社区</a>
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

  <b>◆ 2026年，作为社区重要的生态协同推动落地，我们迎来了第一位伙伴——<a href="https://github.com/dataelement">Dataelem（数据项素）社区</a>，依托“工作台”这一可能在 AI 应用产品化中成为 cornerstone 的产品形态，加速建立“装好就能用，自带全程病情管理体系”的全新产品。</b><br /><br />

  <b>✧ 毫无疑问，我们在未来 3 个月内，将成为 GitHub 和开源中，肿瘤与罕见病患者公益开源工具领域的一股推动力量。期待您加入，Mark the Dent，期待和开发者们一起为患者信息平权做出改变。这是一个因为参与而为千万人带来命运改变的HVT项目。</b>
</p>

<br /><br />
<h2 align="center"><b>项目宣言</b></h2>
<p align="left">

  <b>✦ 通过与 DSH Desktop 的紧密协作，我们致力于为 40+ 癌症、200+ 罕见病群体打造“开箱即用、自带全程病情管理体系”的新一代 AI Agent 能力，帮助患者整理病程资料、追踪指标并做好就诊准备。</b><br /><br />

  <b>◆ 我们相信，技术的价值不只是提高效率，而是让每一个患者都能获得更好的信息、更多的选择与更有尊严的照护体验。</b><br /><br />

  <b>✧ 因此，我们通过开放开发脚手架、插件生态扩展，诚邀开源社区中所有愿意为患者信息与福祉带来改变的开发者、研究者与伙伴，一起推动这项温暖而有意义的事业。</b>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/xyb-openharness-dsh-plugins/.github/main/profile/assets/community-banner.png" alt="小X宝社区横幅" width="860" />
</p>

<p align="center">
  <a href="https://info.xiao-x-bao.com.cn">小X宝社区</a> ·
  <a href="https://www.xiaoyibao.com.cn">小胰宝官网</a> ·
  <a href="#社区仓库">社区仓库</a> ·
  <a href="#文档导航">文档</a> ·
  <a href="#贡献指南">贡献</a> ·
  <a href="#联系方式">联系我们</a>
</p>

> [!IMPORTANT]
> **当前发布版本不是“全部病种开箱即用”。**
> 罕见病与部分社区尚未覆盖的癌种，仍在骨架、设计或招募阶段；已发布工作台的成熟度也不一致。
> 首个版本的目标不是交付成品，而是给**熟悉病情管理逻辑、愿意一起做的罕见病社区伙伴、开发者、患者家属、志愿者**一个可上手的台阶，一起把产品做得更好。
> 先看 [PROJECTS.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/PROJECTS.md) 与 [BACKLOG.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md) 确认病种状态，再选择试用、认领或共建。

---

## 目录

- [项目概述](#项目概述)
- [当前版本边界与共建邀请](#当前版本边界与共建邀请)
- [适合谁](#适合谁)
- [主要特性](#主要特性)
- [架构一览](#架构一览)
- [我们最需要的能力（招募）](#我们最需要的能力招募)
- [快速开始](#快速开始)
  - [系统要求](#系统要求)
  - [安装](#安装dsh-desktop推荐路径)
  - [验证安装](#验证是否真的装上)
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

**OpenHarness DSH Plugins** 是小X宝社区与 [Dataelem（数据项素）](https://github.com/dataelement) 合作建设的患者工作台与插件社区。工作台运行于由 Dataelem 维护的 [DSH Desktop](https://github.com/dataelement/dsh-desktop)，围绕患者的真实场景组织资料、病程和就诊准备。

**DSH Desktop by Dataelem** 是由 Dataelem 团队基于上游 [DeepSeek Harness](https://github.com/deepseek-ai/dsh) 开发的桌面 Agent 应用；它不是 DeepSeek 官方桌面产品。小X宝社区贡献患者场景与业务经验，Dataelem 提供桌面宿主、工作台框架和产品化支持，双方共同完善样板与可复用脚手架。

我们以「**公益与开源**」为核心，旗舰项目 **小胰宝（XiaoYiBao）** 与各病种工作台聚焦信息整理、病程记录、指标追踪与就诊准备，帮助患者和家属更清楚地管理资料与沟通问题。工作台不提供诊断、治疗或处置建议，不替代医生判断。

**核心目标：**

- **开放生态**：面向研究者、临床工程师与开发者开放，任何人都可以基于统一规范贡献插件。
- **安全可解释**：输出带有支持性证据与参考来源，隐私优先，避免可识别信息泄露。
- **高度可扩展**：模块化插件机制，便于接入新模型、新数据源与新场景。
- **社区驱动**：鼓励临床、研究与开发者共同参与，让技术成为连接人与希望的桥梁。

---

## 当前版本边界与共建邀请

### 先说清楚：不是全部病种都开箱即用

- **罕见病与部分社区尚未覆盖的癌种**：仍在骨架、设计或招募阶段，功能与内容不完整。
- **已发布工作台**：成熟度也不一致；有的可以日常使用，有的只是可点通的初版。
- **不同工作台**：数据模型、字段、导入/解析能力可能不同；以各自 README 与 [PROJECTS.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/PROJECTS.md) / [BACKLOG.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md) 的状态为准。

### 成熟度标记

| 标记 | 含义 |
| --- | --- |
| 🟢 | 社区初期版本可用：核心流程可走通，已有社区使用，仍在持续迭代 |
| 🔵 | 开发中：主要功能已落地，仍在真机迭代 |
| 🟡 | 设计中 / 初版：骨架或原型，流程尚未完整 |
| ⚪ | 已认领，待开工 |
| ⬜ | 招募中：尚无固定维护者 |

### 产品能力约束（先读）

- **不是医疗器械**：不做诊断、治疗建议或疗效判断，不替代医院系统与医生。
- **解析成功 ≠ 结构化成功**：MinerU/OCR 受原件质量、Token/同意、文档类型影响；可能 0 候选，需要看解析文本或人工补录。
- **AI 只做“读并提议候选”**：不直接写事实库；接受/修改/拒绝由人完成。
- **AI 自动入库尚未闭环**：公开会话合同只有草稿与发送，没有完成回复事件；当前是“手动导入/粘贴回复”，宿主补 `completed` 事件后才做自动解析。
- **知识库、批量导入、多文件、AI 抽取仍在迭代**：不是所有工作台都有。
- **数据默认本机**：云解析/外部 API 需用户同意，并说明发送范围。
- **病种覆盖不完整**：不要把它当成“所有病种都能直接用”的产品。

### 首个版本的目标：给共建者一个台阶

我们希望它不是“成品发布会”，而是一个**可上手的台阶**：

- **罕见病社区伙伴**：带着病种知识来，补流程、字段、话术和真实场景。
- **开发者**：补模块、接 OCR/MinerU/知识库/API，修 bug。
- **患者家属 / 志愿者**：试用、访谈、校对内容、组织培训；不需要写代码也能贡献。
- **医护 / 研究者**：校对医学逻辑，指出不该做、不能做的边界。

从哪里开始：[PROJECTS.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/PROJECTS.md) 看已开工病种 → [BACKLOG.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md) 看缺口与认领 → [CONTRIBUTING.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/CONTRIBUTING.md) 选路径 → [CONTRIBUTING-WORKBENCH.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/CONTRIBUTING-WORKBENCH.md) 看闸口与 PR 自检。

---

## 适合谁

| 人群 | 适合做什么 | 说明 |
| --- | --- | --- |
| **有一定技术能力的患者/家属** | 自建档案、导入病历、整理指标、准备就诊问题 | 默认推荐；需要会选资料目录、安装插件 |
| **社区志愿者** | 经过集中培训后，帮助病友建档、导入、核对 | 重点人群；培训后可批量帮扶，降低患者上手门槛 |
| **医护团队** | 二次开发、校对字段与流程、病种差异化 | 不做诊疗决策，只做资料整理与就诊准备 |
| **代诊/陪诊人员** | 帮患者把资料整理成就诊材料 | 需患者授权；遵守隐私与数据保护要求 |
| **病友组织/运营团队** | 认领病种、组织内容访谈、培训与试用 | 不需要写代码也能贡献；见 [CONTRIBUTING-WORKBENCH.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/CONTRIBUTING-WORKBENCH.md) |

许可：本组织推荐/默认 **MIT**；历史仓库以各自 `LICENSE` 为准。

> 工作台只做信息整理与就诊准备，**不提供诊断、治疗建议或疗效判断**。

---

## 主要特性

1. **DSH Desktop 工作台** —— 通过桌面宿主承载病种业务面板与插件能力。
2. **患者场景驱动** —— 以「小胰宝」等病种工作台为样板，持续完善患者与家属的信息管理流程。
3. **来源可追溯** —— 医学内容标注来源与版本，未核实项明确标注，不生成诊疗建议。
4. **病历与指标整理** —— 围绕病程、检查资料和就诊问题建设整理能力；具体支持范围以各工作台说明与验证状态为准。
5. **可扩展插件机制** —— 通过 `cordis.patch.yml` 的 `insert` 入口或 DSH 的插件安装入口接入第三方插件；在 DSH Desktop 内一律走 app 的工作台市场 / 已安装列表，不另起 Web 界面。
6. **多语言与本地化** —— 内置中文本地化，文档与界面支持持续扩展更多语言。

---

## 架构一览

**工作台为核心，向下接基础能力，向上承载端应用；AI 与工作台双向，MinerU 只负责解析。**

```text
┌────────────────────────────────────────────────────────────────────┐
│ 端应用层                                                           │
│   Harness Web UI（Desktop 内；独立 Web 需单独部署）                │
│   DSH Desktop（工作台面板） · 未来：手机/小程序（依赖宿主 API）     │
└───────────────────────────────┬────────────────────────────────────┘
                                │
┌───────────────────────────────▼────────────────────────────────────┐
│ 工作台核心                                                         │
│   壳层：customFrame / 原生会话绑定 / 权限与审计                     │
│   业务：多档案 · 病程与指标 · 资料整理 · 就诊准备 · 候选核对 · 导出 │
│         心理支持（陪伴 → 安宁疗护 → 哀伤管理）· 营养支持 · 临床匹配 │
│         药物查询 · 并发症管理 · 更多场景（持续扩展）                │
└───────┬───────────────────┬───────────────────┬────────────────────┘
        │ 双向              │ 原件/批量         │ 检索/索引
┌───────▼────────┐  ┌───────▼────────┐  ┌───────▼────────┐
│ AI 集成        │  │ MinerU（外部） │  │ 知识库（本地） │
│ 原生会话       │  │ OCR/版面/表格  │  │ 文件 + FTS5    │
│ 后台任务待定   │  │ markdown/JSON  │  │ 未来向量检索   │
└───────┬────────┘  └───────┬────────┘  └───────┬────────┘
        │                   │                   │
┌───────▼───────────────────▼───────────────────▼────────────────────┐
│ 未来 API：knows API · XYB RAG API · OCR 多通道 · 心理/营养/影像/基因 │
└────────────────────────────────────────────────────────────────────┘
```

- **AI ↔ 工作台**：工作台把提示词、已确认事实、检索片段交给原生会话；AI 只回候选/解释，不直接写事实库。
- **MinerU 链路**：原件 → MinerU 批量解析 → markdown/content_list → `parsed/<docId>.md` + 候选 → 人工确认 → SQLite 事实层。
- **运行时**：这是逻辑分层，不是进程图；工作台是 profile 内的 DSH 插件——服务端在 Harness 进程，Panel 在 Harness Web UI，业务页在 iframe，原生会话由宿主传入；资料在工作台自己的 workspace。详见 [ARCHITECTURE.md §2.2](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/ARCHITECTURE.md#22-运行时映射工作台作为-dsh-插件)。
- **数据面**：工作台 SQLite 在用户选择的资料目录（如 `pinkypal.sqlite`），不在 DSH profile，也不在会话库；AI 不直接打开它。
- **AI 写回**：AI 回复只做候选，经工作台 API + 人工确认后才写 SQLite；默认不提供 SQL/代码写工具，不改前端。
- 完整架构、AI 写 SQLite 的底层路径见 **[ARCHITECTURE.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/ARCHITECTURE.md)**。

---

## 我们最需要的能力（招募）

| 能力 | 需要谁 | 具体做什么 |
| --- | --- | --- |
| **MinerU 融合** | MinerU 原厂 / 解析高手 | 让 PDF/图片/表格抽取更快、更准、更简单：批量解析、表格对齐、跨页结构、失败重试 |
| **OCR 多通道** | 熟悉 OCR 工具/项目的开发者 | 接入 DeepSeek-OCR2、GLM-OCR、PaddleOCR-VL-1.5、Youtu-Parsing、Indra OCR、macOS Vision、云 OCR 等；统一输出 `text/pageRef/tables`，用户可切换；选型表与魔搭地址见 [CONTRIBUTING §2.2](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/CONTRIBUTING.md#22-其它-ocr-工具与项目多通道) |
| **罕见病/肿瘤社区开发者与运营** | 病种社区、病友组织、一线患者 | 补病情管理逻辑与细节、校对内容、组织培训与试用；当前版本与真实应用仍有差距 |
| **开源技术力量与公益 API 提供方** | API/能力提供方 | 心理咨询、营养咨询、医疗知识库、医学影像、基因解读（如 KHUB OpenGene）、knows API、XYB RAG API |

入口：Issue 模板或 [CONTRIBUTING.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/CONTRIBUTING.md)；病种认领见 [BACKLOG.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md)。

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

1. 从 [DSH Desktop 官网](https://dshdesktop.com/zh/)安装并启动 **DSH Desktop**，完成首次引导。
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
| **小胰宝 XiaoYiBao** | 官方 · 医疗 | 面向患者与家属的病程资料整理、指标追踪与就诊准备 | 已发布 |
| [xyb-workbench-starter](https://github.com/xyb-openharness-dsh-plugins/xyb-workbench-starter) | 社区 · 脚手架 | 用于创建符合本组织规范的 DSH Desktop 患者工作台 | 已提供，持续迭代 |
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

我们正在为一个个具体病种建设「本机优先」的患者工作台（病程整理 · 指标追踪 · 就诊准备，不静默上传患者数据，调用外部模型或服务时需明确说明发送内容）。目标池参照 **NCCN Guidelines® 病种目录（67 个条目）** 与 **《86 个罕见病病种诊疗指南（2025 年版）》**（合计 **153 项**），聚焦让患者能自主管理、医生可快速复盘和协作。

**153 个目标不是 153 次全流程**：按 `T0 家族样板 / T1 标准 / T2 模板化 / T3 挂靠 / T4 观察池` 分级，按波次推进，每波结束留 1–2 周回流窗口把经验沉淀进脚手架。详见 [PROGRAM-PLAN.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/PROGRAM-PLAN.md)。

**已启动 38 个工作台**（截至 2026-10-26：28 个癌种线 + 9 个罕见病 + 1 个跨病种心理支持；🔵 开发中 / 🟡 设计中 / 🟢 社区初期版本可用，完整状态与认领方式见 [BACKLOG.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md)）：

| 病种工作台 | 进度 | 仓库 |
| --- | --- | --- |
| 乳腺癌 · 小粉宝 PinkyPal | 🔵 v0.12.0（G1–G3 已过） | [breast-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/breast-cancer-workbench) |
| 淋巴瘤 · 小铃铛 LymBell | 🔵 v0.3.0 | [lymphoma-workbench](https://github.com/xyb-openharness-dsh-plugins/lymphoma-workbench) |
| 卵巢癌 · 小巢宝 | 🔵 v0.1.51 | [ovarian-workbench](https://github.com/xyb-openharness-dsh-plugins/ovarian-workbench) |
| 肺癌 · 小肺宝（NSCLC + SCLC 已合并） | 🔵 v0.1.2-rc.16 | [lung-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/lung-cancer-workbench) |
| 胰腺癌 PDAC · 小胰宝（历史旗舰） | 🔵 v0.1.34 | [xyb-workbench](https://github.com/xyb-openharness-dsh-plugins/xyb-workbench) |
| 结直肠癌 · 小畅宝 Colopal（消化族样板） | 🟡 v0.1.0 | [colorectal-workbench](https://github.com/xyb-openharness-dsh-plugins/colorectal-workbench) |
| 胃癌 · 小胃宝 Stompal | 🟡 v0.1.0 | [gastric-workbench](https://github.com/xyb-openharness-dsh-plugins/gastric-workbench) |
| 食管癌 · 小咽宝 EsopPal | 🟡 v0.1.0 | [esophageal-workbench](https://github.com/xyb-openharness-dsh-plugins/esophageal-workbench) |
| 宫颈癌 · 小莲宝 CerviPal | 🟡 v0.1.1 | [cervical-workbench](https://github.com/xyb-openharness-dsh-plugins/cervical-workbench) |
| 肛管癌 · 小萌宝 AnalPal（10-21 认领） | 🔵 v0.2.0（G2 已签） | [anal-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/anal-cancer-workbench) |
| 胃肠间质瘤 · 小吉宝 GistPal（10-21 认领） | 🟡 v0.1.0 | [gist-workbench](https://github.com/xyb-openharness-dsh-plugins/gist-workbench) |
| 肝细胞癌 · 小甘宝 HepPal（10-24 认领） | 🔵 v0.3.6（G1–G3 已签认） | [liver-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/liver-cancer-workbench) |
| 胆道癌（10-24 认领） | 🟡 v0.1.0（本地脚手架，远端仓待建） | — |
| 胶质母细胞瘤 · 小星宝 StarPal（10-24 认领，独立建仓） | 🔵 v0.1.5 | [glioblastoma-workbench](https://github.com/xyb-openharness-dsh-plugins/glioblastoma-workbench) |
| 恶性胸膜间皮瘤（10-24 认领） | 🔵 v0.1.4 | [mesothelioma-workbench](https://github.com/xyb-openharness-dsh-plugins/mesothelioma-workbench) |
| 膀胱癌 · 小泉宝 UroPal（10-23 认领） | 🔵 v0.1.0（G1–G3 已签） | [bladder-workbench](https://github.com/xyb-openharness-dsh-plugins/bladder-workbench) |
| 前列腺癌（T0 泌尿样板，10-22 认领） | 🟡 v0.1.0 | [prostate-workbench](https://github.com/xyb-openharness-dsh-plugins/prostate-workbench) |
| 甲状腺癌（10-24 认领） | 🔵 v0.2.1 | [thyroid-workbench](https://github.com/xyb-openharness-dsh-plugins/thyroid-workbench) |
| 肾癌 · 小肾宝 RenalPal（10-22 认领） | 🔵 v0.3.0（G1 已签） | [kidney-workbench](https://github.com/xyb-openharness-dsh-plugins/kidney-workbench) |
| 皮肤黑色素瘤 · 小痣宝 MolePal（T0 样板，10-25 认领） | 🔵 v0.3.1 | [melanoma-workbench](https://github.com/xyb-openharness-dsh-plugins/melanoma-workbench) |
| 头颈癌 · 小嗓宝 VoicePal（T0 样板，10-25 认领） | 🔵 v0.1.6 | [head-neck-workbench](https://github.com/xyb-openharness-dsh-plugins/head-neck-workbench) |
| 软组织肉瘤（T0 样板，10-25 认领） | 🟡 v0.1.0 | [sarcoma-workbench](https://github.com/xyb-openharness-dsh-plugins/sarcoma-workbench) |
| 多发性骨髓瘤 · 小浆宝 MyeloPal（10-25 认领） | 🟡 v0.1.0 | [myeloma-workbench](https://github.com/xyb-openharness-dsh-plugins/myeloma-workbench) |
| 子宫内膜癌 · 小膜宝 EndoPal（10-25 认领） | 🔵 v0.3.2 | [endometrial-workbench](https://github.com/xyb-openharness-dsh-plugins/endometrial-workbench) |
| 慢性粒细胞白血病 · 小粒宝 GranPal（T0 血液样板，10-25 认领） | 🟡 v0.1.0 | [cml-workbench](https://github.com/xyb-openharness-dsh-plugins/cml-workbench) |
| CLL/SLL · 小淋宝 LymPal（10-25 认领） | 🔵 v0.7.0 | [cll-workbench](https://github.com/xyb-openharness-dsh-plugins/cll-workbench) |
| 神经内分泌和肾上腺肿瘤 · 小肽宝（10-25 认领） | 🟡 v0.1.0 | [neuroendocrine-workbench](https://github.com/xyb-openharness-dsh-plugins/neuroendocrine-workbench) |
| 妊娠滋养细胞肿瘤 · 小葡宝 GraPal（10-25 认领） | 🔵 v0.5.0 | [gtn-workbench](https://github.com/xyb-openharness-dsh-plugins/gtn-workbench) |
| 罕见病样板 · FSHD 小飞侠 | 🟡 v0.1.1 | [fshd-workbench](https://github.com/xyb-openharness-dsh-plugins/fshd-workbench) |
| 罕见病 · ATTR 淀粉宝宝 ATTR-Pal（10-21 认领） | 🔵 v0.3.1（真机装机迭代中） | [attr-workbench](https://github.com/xyb-openharness-dsh-plugins/attr-workbench) |
| 肢端肥大症 · 小肢宝 LimbPal（R2 样板，10-25 认领） | 🔵 v0.2.3 | [acromegaly-workbench](https://github.com/xyb-openharness-dsh-plugins/acromegaly-workbench) |
| ANCA 相关血管炎 · 小脉宝 VasPal（10-25 认领） | 🟡 v0.1.0 | [anca-vasculitis-workbench](https://github.com/xyb-openharness-dsh-plugins/anca-vasculitis-workbench) |
| 原发性胆汁性胆管炎 · 小管宝 DuctPal（10-25 认领） | 🟡 v0.2.7（G1–G3 待签认） | [pbc-workbench](https://github.com/xyb-openharness-dsh-plugins/pbc-workbench) |
| PF-ILD · 小呼宝 BreathPal（10-25 认领） | 🔵 v0.2.1（G1 已签） | [pf-ild-workbench](https://github.com/xyb-openharness-dsh-plugins/pf-ild-workbench) |
| 神经纤维瘤病 · 小纤宝 FibroPal（10-25 认领） | 🔵 v0.1.4 | [neurofibromatosis-workbench](https://github.com/xyb-openharness-dsh-plugins/neurofibromatosis-workbench) |
| 发作性睡病（10-25 认领） | ⚪ 已认领 · 建仓待开工 | （空仓占位） |
| 重型地中海贫血（10-25 认领） | ⚪ 已认领 · 建仓待开工 | （空仓占位） |
| 心理支持 · 小心宝（跨病种共用模块） | 🟢 v0.3.14 | [xiaoxinbao-workbench](https://github.com/xyb-openharness-dsh-plugins/xiaoxinbao-workbench) |
| 其余主要癌种 + 罕见病 | ⬜ **招募认领中**（完整分级与招募对象见 BACKLOG） | [BACKLOG.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md) |

> 🔥 **优先招募榜 12 项已全部认领（截至 2026-10-25）**：[BACKLOG §〇 优先招募榜](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md#〇现在最缺人优先招募榜) 按「帮扶人群规模 · 信息差 · 危重与时间压力」三维挑选的 12 个目标已在 10-21 → 10-25 全部有主。当前最缺的是**已开工工作台的 🩺 医学核对与 👤 患者访谈补位**，以及尚未启动病种的新认领（W2 其余血液肿瘤、W4 皮肤/胸腺、R2/R3 大部分仍 ⬜）。缺什么角色（👤 患者家属 / 🩺 临床 / 💻 开发 / 📝 内容 / 🤝 病友组织 / 👨‍👩‍👧 患儿家长）与第一步能做什么，见 [BACKLOG.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md)。
>
> 🤝 **诚邀加入**：无论你是开发者、临床/研究者、病友组织志愿者还是写作者，都可以认领一个病种或一个模块。四种投入档位（整仓 / 模块 / 内容访谈 / 脚手架）见 **[CONTRIBUTING-WORKBENCH.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/CONTRIBUTING-WORKBENCH.md)**，从 Issue 模板开始。**不需要写代码也能贡献**——一次真实经历访谈、一份就诊问题清单都在缺。所有工作台只做信息整理，不做诊断建议。
>
> 🔒 **仓库可见性**：病种工作台一律 private（仅本组织 public 仓库与 `xyb-workbench-starter` 可公开浏览），因此上表里的病种仓库链接对组织外访客会 404，属预期。**每个项目的公开展示页（原型首页截图 + 能力说明）在 [PROJECTS.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/PROJECTS.md)**，外部贡献者的协作方式：**Issue 层认领与评审不需要任何权限**，需要写代码时再由维护者逐人最小授权（见 [CONTRIBUTING §10.3](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/CONTRIBUTING-WORKBENCH.md)）。

---

## 文档导航

- **架构说明**（三层架构 / AI 双向 / MinerU 链路 / AI 写 SQLite）：[ARCHITECTURE.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/ARCHITECTURE.md)
- **开发与贡献指南**（环境 / 合同 / 接入能力 / 测试 / 发布）：[DEVELOPMENT.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/DEVELOPMENT.md)
- **安装与验证**（市场/命令行安装、三层验收、排错）：[INSTALL.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/INSTALL.md)
- **使用说明**（适合谁 / 第一次使用 / 多档案 / 解析核对）：[USAGE.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/USAGE.md)
- **贡献入口**（角色 / 四条路径 / 最需要的能力）：[CONTRIBUTING.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/CONTRIBUTING.md)
- **快速开始**：见上方 [快速开始](#快速开始)
- **项目画廊**（首批 14 个项目的原型截图与能力说明；其后新开工 20+ 个见各病种认领 Issue 与 [BACKLOG.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md)）：[PROJECTS.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/PROJECTS.md)
- **插件开发指南**：见下方 [插件开发](#插件开发)
- **患者工作台脚手架**：[xyb-workbench-starter](https://github.com/xyb-openharness-dsh-plugins/xyb-workbench-starter)
- **患者工作台路线图与病种认领**：[ROADMAP.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/ROADMAP.md)
- **规模化开发总纲**（分层分级 / 波次 / 七道质量锁）：[PROGRAM-PLAN.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/PROGRAM-PLAN.md)
- **153 项目标池分层表、招募对象与认领状态**：[BACKLOG.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md)（含 [§〇 优先招募榜](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/BACKLOG.md#〇现在最缺人优先招募榜)）
- **脚手架迭代与经验回流**：[SCAFFOLD-ITERATION.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/SCAFFOLD-ITERATION.md)
- **贡献手册（四条路径 / 闸口 / PR 自检）**：[CONTRIBUTING-WORKBENCH.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/CONTRIBUTING-WORKBENCH.md)
- **贡献流程**：见下方 [贡献指南](#贡献指南)
- **项目结构**：见下方 [项目结构](#项目结构)
- **小胰宝官网**：<https://www.xiaoyibao.com.cn>
- **小X宝社区**：<https://info.xiao-x-bao.com.cn>
- **OpenCare SkillHub 社区仓库**：<https://github.com/opencare-skillhub>
- **PancrePal（小胰宝）社区仓库**：<https://github.com/PancrePal-xiaoyibao>
- **Dataelem 官网**：<https://www.dataelem.com/>
- **DSH Desktop 官网**：<https://dshdesktop.com/zh/>
- **DSH Desktop 源码（Dataelem）**：<https://github.com/dataelement/dsh-desktop>
- **DSH 工作台资源**：<https://github.com/dataelement/awesome-dsh-workbench>
- **上游 DeepSeek Harness**：<https://github.com/deepseek-ai/dsh>
- **cordis 插件框架**：<https://github.com/cordiverse/cordis>

> 更完整的 Wiki / API 文档链接将随生态完善逐步补充，欢迎认领文档建设。

---

## 项目结构

本组织采用「元仓库（`.github`）+ 各插件独立仓库 / 子目录」的组织方式：

```text
xyb-openharness-dsh-plugins/
├── .github/                      # 组织元仓库
│   ├── profile/README.md         # 组织首页
│   ├── PROGRAM-PLAN.md           # 开发总纲
│   ├── BACKLOG.md                # 目标池与招募
│   └── CONTRIBUTING-WORKBENCH.md # 贡献手册
├── xyb-workbench-starter/        # 患者工作台脚手架（独立仓库）
└── <病种>-workbench/              # 各病种工作台（独立仓库）
```

> 各仓库的具体文件、访问权限与许可证以对应仓库为准。

---

## 贡献指南

我们欢迎一切形式的贡献：代码、文档、翻译、Issue 反馈与插件孵化。

**患者工作台的详细贡献手册见 [CONTRIBUTING-WORKBENCH.md](https://github.com/xyb-openharness-dsh-plugins/.github/blob/main/CONTRIBUTING-WORKBENCH.md)**，含四条贡献路径（病种认领 / 模块 / 内容与医学核对 / 脚手架）、三闸口、PR 自检清单与评审清单。

### 贡献流程

1. **认领或提出议题**：在 [Issues](https://github.com/xyb-openharness-dsh-plugins/.github/issues) 中搜索或新建议题，讨论需求与方案；认领病种请用「病种认领」模板，并在 Issue 下评论 `/claim` 完成领取。
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

提交贡献前，请确认目标仓库实际公布的许可证与贡献条款，并确认你有权据此授权；未公布许可证的仓库请先联系维护者确认。

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
- **GitHub Issues**：用于缺陷反馈与功能建议 —— [组织议题](https://github.com/xyb-openharness-dsh-plugins/.github/issues)
- **GitHub Discussions**：用于想法交流与新插件提案（如已开启）
- **邮件**：opensource@xiaoyibao.com.cn（请以实际公布地址为准）

---

## 许可证和免责声明

### 许可证

本组织推荐/默认采用 **MIT** 协议；历史仓库与实际发布包以其各自 `LICENSE` 为准。使用、修改或分发前，请查看目标仓库的许可说明；未单独声明的仓库请联系维护者确认。

### 免责声明

- **非医疗建议**：本组织提供的插件（尤其是「小胰宝」等医疗相关插件）所生成的内容**仅供研究与信息参考，不构成任何形式的专业医疗诊断、治疗建议或诊疗决策**。
- **AI 生成内容**：插件输出由人工智能模型生成，可能存在错误或偏差，使用前请自行核验关键信息与引用来源。
- **隐私优先**：使用涉及个人健康信息的功能时，请遵循所在地区的数据保护法规，避免上传可识别个人身份信息；本组织不对因误用导致的信息泄露承担责任。
- **责任限制**：在适用法律允许的最大范围内，本组织及其贡献者对使用本组织插件产生的任何直接或间接损失不承担责任。

---

<p align="center">
  用技术守护生命，用开源连接希望 —— 欢迎加入 OpenHarness DSH Plugins。
</p>
