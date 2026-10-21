# 脚手架迭代与经验回流机制

> 脚手架仓库：[xyb-workbench-starter](https://github.com/xyb-openharness-dsh-plugins/xyb-workbench-starter)（当前包版本 1.4.3，CLI `dsh-wb-cli`）。
> 上游原则见其 `docs/MAINTENANCE.md`（"一个规则只在一个位置维护"、"将稳定经验上提到 AGENTS 前先看是否只是个案"）。本文把它扩展成 **150+ 个病种规模下的可执行回流流程**。
> 更新日期：2026-10-21。

---

## 0. 核心矛盾

病种越多，脚手架越容易两极分化：

- **不动** → 每个新病种重复踩同样的坑，质量随数量线性劣化。
- **乱动** → 每个病种都往 starter 塞一条特例，脚手架变成病历本，且已生成项目被静默改变行为。

解法：**三档上提门槛 + 双病种复现验收 + 已生成项目不自动跟随**。

---

## 1. 三档上提（回流的目的地决定门槛）

| 档 | 目的地 | 上提门槛 | 审批 | 版本影响 |
| --- | --- | --- | --- | --- |
| **L1 项目层** | 病种仓库 `docs/LESSONS.md` | 无门槛，每次故障/返工必记 | 无 | 无 |
| **L2 能力层** | starter `docs/NN-*.md`、`prompts/`、`templates/`、`scripts/` | 该经验在 **≥2 个病种**独立复现，且能用模板/提示词/检查项表达 | 1 名维护者 review | minor（新增能力） |
| **L3 硬约束层** | starter `AGENTS.md`、`scripts/check-starter.mjs`、冻结合同 | 该规则被违反过 **≥2 次**并造成实际事故；且能自动化拦截 | 维护者 + 至少 1 个真实项目回归 | major（若改变既有行为）+ 迁移说明 |

**判定口诀**：
- 只有一个病种遇到 → 留在 L1（可能只是个案）。
- 两个病种都遇到且形态一致 → 上提到 L2。
- 上提后仍有人违反 → 升级为 L3，写成检查项自动拦截。

---

## 2. 回流包（Reflow Pack）：一个 PR 里必须有什么

波末回流窗口产出的 PR 至少包含：

```text
reflow/<波次>-<主题>/
├─ docs/NN-<主题>.md            新增或修订能力文档（写明适用边界）
├─ prompts/<名字>.md            若产出可复用提示词
├─ templates/...                若产出可复用模板/骨架
├─ scripts/check-*.mjs          若新增自动检查（附失败示例）
├─ CHANGELOG.md                 顶部一条：来源病种、问题、修复、适用范围
├─ package.json / VERSION       semver 递增（见 §4）
└─ 验收记录（PR 描述内）：
   ├─ 来源病种 A / B（两个，注明版本与 commit）
   ├─ 复现步骤与原始错误
   ├─ 临时目录同配置重新生成的 diff 摘要
   └─ 至少 2 个真实项目回归结果（npm run check / npm test）
```

**缺"两个来源病种"的回流 PR 一律打回。** 单病种经验只能进 L1。

---

## 3. 回流验收流程（不可跳过任何一步）

```bash
# 1. 在临时目录用相同配置重新生成，比较模板与规则差异（不整目录覆盖业务项目）
mkdir -p /tmp/reflow-check && cd /tmp/reflow-check
dsh-wb-cli init <probe>-workbench --config <已确认配置>.json
diff -r <probe>-workbench <既有真实项目的关键模板文件>

# 2. 脚手架自身检查
cd <starter克隆>
npm run check
npm test

# 3. 至少两个真实病种项目回归
cd <病种A> && npm run check && npm test
cd <病种B> && npm run check && npm test

# 4. 通过后才打 tag
git tag -a v1.5.0 -m "reflow: <主题>（来源：A、B）"
```

**验收记录写进 PR 描述**，同时同步 starter `docs/GIT-SYNC-<日期>.md`。
跑测试/装包前先 `NODE_OPTIONS=`（置空），否则宿主 shim 会制造假失败。

---

## 4. 版本与 tag 策略

| 变更类型 | 版本 | 要求 |
| --- | --- | --- |
| 修文档/错别字、补例子 | patch | CHANGELOG 一条 |
| 新增能力（新提示词/新模板/新检查项） | minor | 验收见 §3，至少 1 个真实项目回归 |
| 改变既有行为（改 AGENTS 约束、改模板输出、改检查项判定） | **major** | 必须附**迁移说明**：老项目会看到什么差异、要不要手工处理 |
| 未发布的实验改动 | 不打 tag | 在分支验证，合入 `main` 后才 tag |

- `VERSION`（或 `package.json` 版本）是唯一来源，`CHANGELOG.md` 顶部必须同步一条；**改了版本头不记 CHANGELOG 视为未完成**（这条纪律来自社区技能维护的既有教训）。
- 固定版本可用 tag checkout；`detached HEAD` 可用于 `init`，但 `sync` 会因无 upstream 停止。
- `npm link` 激活的 CLI，更新克隆后无需重新激活（除非 bin 声明或依赖变化）。

---

## 5. 已生成项目：不自动跟随

- 每个业务项目根目录的 `.dsh-wb-starter.json` 记录 **CLI 版本 + Git commit + dirty 状态 + 生成时间**。这是判断"项目按哪版脚手架验过"的唯一依据。
- `dsh-wb-cli sync` **只更新 starter 克隆**，绝不修改业务项目。
- 业务项目要跟进新版脚手架，走**显式升级**：在临时目录同配置生成 → 人工 diff → 挑选需要的模板/规则 → 更新 `.dsh-wb-starter.json` 的来源记录 → 跑完整检查链与 V2 装机复验。
- **禁止整目录覆盖**。历史快照保留，不能静默覆盖后声称旧项目按新版验过。

### 升级窗口建议

| 项目状态 | 是否建议跟进新版 |
| --- | --- |
| 已 🟢 发布、无新增需求 | 不跟进，只在下次有需求时一并处理 |
| 🔵 开发中 | 波末窗口评估，只对"修 bug 类"更新跟进 |
| 🟡 设计中（G2 未签） | 建议跟进，成本最低 |
| 刚 init 未开工 | 直接重建 |

---

## 6. 波末回流窗口（1–2 周做什么）

1. **收**：本波每个病种的 `docs/LESSONS.md` 逐条过，标注"个案 / 可复用"。
2. **判**：可复用的按 §1 三档定目的地；不满足两个来源的退回 L1。
3. **写**：按 §2 组回流包。
4. **验**：按 §3 跑临时目录生成 + 两个真实项目回归。
5. **发**：CHANGELOG + 版本 + tag，更新 `docs/GIT-SYNC-<日期>.md`。
6. **审**：跑一次**家族一致性审计**（PROGRAM-PLAN §6.1，8 项），差异列成 issue 分派。
7. **同步**：更新 `BACKLOG.md` 状态与 `ROADMAP.md`。

**回流窗口内不开工新病种。** 这条是硬约束——否则回流永远排在后面，能力债越滚越大。

---

## 7. 已知的反模式（见到即打回）

| 反模式 | 为什么错 |
| --- | --- |
| 一个病种遇到坑就改 starter | 可能只是个案，会污染所有项目 |
| 把病种特有逻辑写进 starter 模板 | 脚手架变病历本；正确做法是写进该病种的 domain pack |
| 改了 starter 但没跑两个真实项目回归 | 无法证明"可复用" |
| 静默改 AGENTS 硬约束 | 老项目行为被改且无迁移说明 |
| 把"npm run check 通过"当作回流验收完成 | 只是包级；必须通过临时目录生成 + 真实项目回归 |
| 在业务项目里手改 starter 生成的文件 | 下次升级必然冲突；要么改模板，要么明确列为项目自有文件 |
| 用 `sync` 后声称业务项目已升级 | `sync` 只更新克隆 |

---

## 8. 快速命令参考

```bash
# 首次部署（每台机器一次）
git clone https://github.com/xyb-openharness-dsh-plugins/xyb-workbench-starter.git
cd xyb-workbench-starter && npm link --ignore-scripts --no-audit --no-fund
dsh-wb-cli doctor

# 新病种开工
dsh-wb-cli init --prepare                    # 生成 project.config.json
dsh-wb-cli init <name>-workbench --dry-run   # 先看会生成什么
dsh-wb-cli init <name>-workbench
cd <name>-workbench && dsh-wb-cli check

# 日常同步（只更新 starter 克隆）
dsh-wb-cli sync --dry-run && dsh-wb-cli sync

# 打包（业务项目内，先按项目要求构建）
dsh-wb-cli pack --dry-run && dsh-wb-cli pack
```

> `init` 只生成文档与骨架，**不代表业务已实现，也不代表 Desktop 已加载**。装机是独立步骤（V2）。

---

## 9. 已上提记录（回流登记）

| 日期 | 档位 | 经验 | 两个来源病种（缺一打回） | 落到 starter 哪里 | 验收 |
| --- | --- | --- | --- | --- | --- |
| 2026-10-21 | **L2 能力层** | 「装到哪个 profile」不能按目录名猜：DSH Desktop 0.12.0 实际加载 app 自己的 Harness（`~/Library/Application Support/dsh-desktop/harness/profiles/web`），`~/.dsh/profiles/*` 是 CLI 侧、Desktop 不读；用户侧入口是设置 → 通用开「启用工作台功能」→ 工作台市场安装 → 重启 Harness → 市场「已安装」核对；验收分配置/列表/界面三层，缺界面层只能写"配置已加载、UI 未验证"；`dsh web` + 浏览器 Settings → Plugins 不是 Desktop 的用法 | ① 肺癌（`docs/DEVELOPMENT-RETRO.md`：装到 `~/.dsh/profiles/web` 后切换器没有该工作台）② 结直肠（`docs/RELEASE.md` / `check-install.mjs`：把 CLI desktop profile 当成 Desktop 的） | `docs/06-VALIDATION-AND-RELEASE.md` 新增「用户侧入口与三层验收」；`project-template/scripts/check-install.mjs`（新项目自带只读自检，自动探测 Harness 并打印判定依据） | 临时目录 `init` 生成 136 文件含该脚本且可运行；胃 / 食管 / 宫颈 / 结直肠四仓回归 `npm run check` 全绿，脚本均正确判定为"未装到 Desktop Harness" |
