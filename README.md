# xyb-openharness-dsh-plugins / `.github`

本仓库是组织 **xyb-openharness-dsh-plugins** 的元仓库（`.github`），用于存放组织级配置与协作模板。

> **组织首页内容位于 `profile/README.md`**，由 GitHub 自动渲染到 <https://github.com/xyb-openharness-dsh-plugins>。
> 直接编辑本文件（根目录 README）不会出现在组织首页。

> [!IMPORTANT]
> **当前发布版本不是“全部病种开箱即用”。** 罕见病与部分社区尚未覆盖的癌种仍在早期阶段；首个版本是给愿意一起做的社区伙伴、开发者、患者家属、志愿者上手的台阶，不是成品发布会。详见 [`profile/README.md`](profile/README.md#当前版本边界与共建邀请)。

## 目录说明

- `profile/README.md` —— 组织 Profile 首页（公开展示内容）
- `ARCHITECTURE.md` —— 三层架构、AI 双向、MinerU 链路、AI 写 SQLite 的底层路径
- `DEVELOPMENT.md` —— 开发与贡献指南（环境、合同、接入能力、测试、发布）
- `INSTALL.md` —— 安装与验证（市场/命令行、三层验收、排错）
- `USAGE.md` —— 使用说明（适合谁、第一次使用、多档案、解析核对）
- `CONTRIBUTING.md` —— 通用贡献入口（角色、四条路径、最需要的能力）
- `CONTRIBUTING-WORKBENCH.md` —— 工作台四条贡献路径、闸口与 PR 自检
- `PROJECTS.md` —— **项目画廊**：全部病种工作台的原型首页截图与能力说明（对外展示入口，链接指向 Issue）
- `BACKLOG.md` / `ROADMAP.md` / `PROGRAM-PLAN.md` —— 目标池、路线图与规模化开发总纲
- `docs/DEVELOPMENT-PROGRESS.md` —— **全局开发进度与待开发清单**（按全新净起盘 / 既有孵化仓续建分类，提交一个更新一次）
- `docs/complication-registry.md` —— **并发症线登记册**（`CX-001`..`CX-014` 去重闸门）
- `assets/projects/` —— 画廊截图
- 其他组织级模板（Issue / PR 模板等，如存在）

如需修改组织首页，请编辑 `profile/README.md` 后提交 PR 并推送到 `main`。

## 病种工作台协作方式

- **内部授权成员**：可以按病种一病一仓，由有组织建仓权限的成员建立独立仓库，再按需授予单仓写权限。
- **新加入的外部开发者**：先在公开孵化仓库 `workbench-incubator` Fork 开发并提 PR，不需要组织建仓权或病种仓库写权限。孵化仓库建立前，可先在认领 Issue 中完成需求讨论和原型准备。
- **孵化项目晋级**：通过需求、差异化和工程检查后，再由维护者择机拆分为独立病种仓；孵化不承诺自动拆仓。
- **双模式领取开发**：
  - **模式 A（0 仓全新净起盘 M0–M7）**：针对 `docs/DEVELOPMENT-PROGRESS.md` 第一、二类（0 Issue + 0 仓库），先跑 `check-claim-guard.mjs` 查重，再提 Issue `/claim`、建私有仓、`init.mjs` 净起盘走完 M0–M7。
  - **模式 B（既有 Issue / 远端 M0–M2 孵化仓接管续建 M3–M7）**：针对第三类（已有认领 Issue 但未建仓）及第四类（13 个 R3 远端 M0–M2 私有孵化仓——非空仓，已有原型但缺 SQLite、服务端与装机），不新建重复 Issue，直接关联原 Issue 并 `git clone` 续建至 M7、发布 `v0.1.0` 并装入 DSH Desktop。
- **进度同步纪律（提交一个更新一次）**：每交付 1 个工作台（或完成一组 2 个并行交付），必须在同一收口步骤同步更新 `BACKLOG.md`、`docs/DEVELOPMENT-PROGRESS.md` 与 `profile/README.md` 并 commit + push。

认领步骤、开发目录约定和验收门槛见 [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md)。
