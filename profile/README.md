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

<h1 align="center">🔥 <a href="https://info.xiao-x-bao.com.cn">小X宝社区</a> &amp; 小胰宝：用 AI 为肿瘤 / 罕见病 / 慢性病患者点亮希望之光 ✨</h1>

<p align="center">
  <b>天工开物旗下公益开源项目（<a href="https://www.xiaoyibao.com.cn">www.xiaoyibao.com.cn</a>）｜关注公众号【小胰宝】官方公众号，以及【小胰宝助手】-知识文章发布获取最新进展</b>
</p>

<p align="center">
  我们深知，代码不仅仅是冷冰冰的字符，更是连接开发者与患者的桥梁，是用技术守护生命的温暖力量。
</p>

<p align="center">
  <img src="assets/community-banner.png" alt="小X宝社区横幅" width="860" />
</p>

<p align="center">
  <a href="https://info.xiao-x-bao.com.cn">小X宝社区</a> ·
  <a href="https://www.xiaoyibao.com.cn">小胰宝官网</a> ·
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

**OpenHarness DSH Plugins** 是一个围绕 [DeepSeek Harness（DSH）](https://github.com/deepseek-ai/dsh) 构建的开源插件组织。DSH 是一套以 [cordis](https://github.com/cordiverse/cordis) 插件加载器为核心、可组合插件栈的 AI Agent 运行框架；本组织负责维护、孵化并聚合运行在 DSH 之上的各类插件。

我们以「**公益与开源**」为核心，旗舰项目 **小胰宝（XiaoYiBao）** 致力于通过 AI 提供诊疗路径支持、共享决策辅导与个性化随访建议，帮助肿瘤、罕见病与慢性病患者及其临床团队做出更好的决策与管理方案。

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
5. **可扩展插件机制** —— 通过 `cordis.patch.yml` 的 `insert` 入口或 `dsh plugin add` 即可接入第三方插件。
6. **多语言与本地化** —— 内置中文本地化，文档与界面支持持续扩展更多语言。

---

## 快速开始

### 系统要求

| 项目 | 最低版本 | 说明 |
| --- | --- | --- |
| Node.js | ≥ 18（推荐 20 LTS） | DSH 运行时依赖 |
| 包管理器 | npm / pnpm | 用于安装 DSH 与插件 |
| Git | 任意较新版本 | 克隆插件与参与贡献 |
| DSH CLI | 最新版 | 见下方安装步骤 |

### 安装

```bash
# 1. 安装 DSH 命令行（具体命令以官方文档为准）
npm install -g @deepseek-ai/dsh

# 2. 确认安装成功
dsh --version

# 3. 进入（或新建）一个 DSH profile 工作区
dsh web --help
```

### 基础使用示例

以启用本组织旗舰插件「小胰宝」为例（请将下方包名替换为你实际使用的插件包名）：

```bash
# 方式一：使用 DSH 自带的插件管理命令
dsh plugin add @xyb/dsh-plugin-xiaoyibao

# 方式二：手动在 profile 的 cordis.patch.yml 中注册（详见「插件开发」）
# profiles/web/cordis.patch.yml
# - insert:
#     - id: xiaoyibao
#       name: '@xyb/dsh-plugin-xiaoyibao'
```

启动 Web 界面后即可在「Settings → Plugins」中看到并开关对应插件：

```bash
dsh web
```

> 提示：若插件是通过本地源码方式安装，请确保包可被当前 profile 的 `node_modules` 解析（软链接或安装到 `profiles/node_modules/@<scope>/<name>`）。

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

## 文档导航

- **快速开始**：见上方 [快速开始](#快速开始)
- **插件开发指南**：见下方 [插件开发](#插件开发)
- **贡献流程**：见下方 [贡献指南](#贡献指南)
- **项目结构**：见下方 [项目结构](#项目结构)
- **小胰宝官网**：<https://www.xiaoyibao.com.cn>
- **小X宝社区**：<https://info.xiao-x-bao.com.cn>
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

### 贡献流程

1. **认领或提出议题**：在 [Issues](https://github.com/xyb-openharness-dsh-plugins) 中搜索或新建议题，讨论需求与方案。
2. **Fork 并创建分支**：从目标仓库的 `main` 切出特性分支，命名如 `feat/your-feature` 或 `fix/your-bug`。
3. **本地开发与自测**：遵循本组织的插件规范与代码风格，确保通过现有检查与基础测试。
4. **提交变更**：提交信息建议遵循 [Conventional Commits](https://www.conventionalcommits.org/)（如 `feat:`, `fix:`, `docs:`）。
5. **发起 Pull Request**：描述改动动机、范围与验证方式；如涉及医疗相关内容，请额外说明安全与隐私考量。
6. **评审与合入**：至少一名维护者评审通过后合入；重要改动可能需要多方确认。

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

将插件安装 / 链接到目标 profile 的 `node_modules` 后，在 `cordis.patch.yml` 中加入一个 `insert` 入口即可加载：

```yaml
# profiles/web/cordis.patch.yml
- insert:
    - id: hello
      name: '@your-scope/dsh-plugin-hello'
```

或者使用 DSH 自带的插件管理命令（推荐）：

```bash
dsh plugin add @your-scope/dsh-plugin-hello
```

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

- **非医疗建议**：本组织提供的插件（尤其是「小胰宝」等医疗相关插件）所生成的内容**仅供研究与信息参考，不构成任何形式的专业医疗诊断、治疗或替代医嘱**。任何健康决策请务必咨询具备资质的医疗专业人员。
- **AI 生成内容**：插件输出由人工智能模型生成，可能存在错误或偏差，使用前请自行核验关键信息与引用来源。
- **隐私优先**：使用涉及个人健康信息的功能时，请遵循所在地区的数据保护法规，避免上传可识别个人身份信息；本组织不对因误用导致的信息泄露承担责任。
- **责任限制**：在适用法律允许的最大范围内，本组织及其贡献者对使用本组织插件产生的任何直接或间接损失不承担责任。

---

<p align="center">
  用技术守护生命，用开源连接希望 —— 欢迎加入 OpenHarness DSH Plugins。
</p>
