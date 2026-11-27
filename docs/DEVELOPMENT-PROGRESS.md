# 工作台全局开发进度与待开发清单（唯一进度跟踪表）

> **更新纪律（提交一个更新一次）**：每完成并提交/发布 1 个病种工作台（或每完成一组 2 个并行交付），必须在同一收口步骤中同步更新以下三处并提交推送：
> 1. 本文件 `docs/DEVELOPMENT-PROGRESS.md`（将对应条目移入已交付区并登记版本号、Issue、Release 与装机状态）；
> 2. `BACKLOG.md`（对应病种状态更新为 `🔵 v0.1.0`）；
> 3. `profile/README.md`（`## 患者工作台路线图` 总表同步新增/更新条目）。

---

## 一、全局盘点总览（截至 2026-11-27）

| 目录范围 | 总条目 | 已建仓/已覆盖 | 待开发 / 待续建说明 |
| --- | --- | --- | --- |
| **NCCN 主要癌种** | 67 项（+1 补充） | **65 项已建仓/已并入** | 仅余 **2 项**已认领但未建仓（`#22 成人 ALL`、`#60 儿童 ALL`）；另有 3 项 T3 挂靠未独立建仓 |
| **罕见病 · R1 肿瘤型（挂靠）** | 20 项 | **19 项已独立建仓或挂靠** | 16 项已独立建仓（含并发在途），3 项已含/在途，仅余 **1 项** `#31 GEP-NET` 未独立建仓 |
| **罕见病 · R2 非肿瘤慢性病型** | 34 项 | **34 项远端仓库已 100% 建立** | 全部已建仓或已交付装机 |
| **罕见病 · R3 儿童/遗传型** | 32 项 | **32 项远端仓库已 100% 建立** | 其中 19 项已交付/在途，**13 项为远端 M0–M2 私有孵化仓**（非空仓，缺 M3–M7 与 DSH 装机） |
| **跨病种 · 并发症线 / 生活服务线** | 14 项（`CX-001`..`CX-014`）+ 生活线 | 2 项已启动（`CX-001` 消化道出血、`CX-005` 恶性肠梗阻 `#175`） | **9 项核心并发症 + 1 项生活服务工作台**完全未认领、无仓 |

> **关于 R2 / R3 孵化仓的重要澄清**：
> 目前罕见病 R2（34 项）与 R3（32 项）的远端仓库已 **100% 建立**。其中 13 个 R3 远端私有孵化仓（`alagille-workbench` 等，Issue `#126`–`#147`）**不是空仓库**，而是已完成 **M0–M2（`init.mjs` + G1 草案 + 单文件静态 HTML 原型）** 的半成品仓，尚缺 **M3–M7（SQLite schema/db、服务端路由、`public/` 生产移植、Puppeteer 实渲截图墙、`v0.1.0` `.tgz` 发布与 DSH Desktop 装机）**。

---

## 二、待开发与待续建任务清单（按领取模式分类）

### 第一类（建议 1-A）：跨病种并发症线 & 生活服务线（0 认领 Issue + 0 仓库，可全新净起盘）

| 编号 | 类型 | 病种 / 主题名称 | 建议仓库名 | 状态 |
| --- | --- | --- | --- | --- |
| **CX-006** | 并发症线（官方第二候选） | 发热性中性粒细胞减少（FN / 粒缺伴发热） | `fn-workbench` | `proposed`（未认领、无仓） |
| **CX-007** | 并发症线 | 静脉血栓栓塞（VTE / 深静脉血栓与肺栓塞） | `vte-workbench` | `proposed`（未认领、无仓） |
| **CX-003** | 并发症线 | 脓毒症 / 严重感染风险（Sepsis） | `sepsis-workbench` | `proposed`（未认领、无仓） |
| **CX-008** | 并发症线 | 急性肾损伤（AKI） | `aki-workbench` | `proposed`（未认领、无仓） |
| **CX-009** | 并发症线 | 消化道穿孔（GI Perforation） | `gi-perforation-workbench` | `proposed`（未认领、无仓） |
| **CX-010** | 并发症线 | 谵妄 / 急性意识改变（Delirium） | `delirium-workbench` | `proposed`（未认领、无仓） |
| **CX-011** | 并发症线 | 疼痛危象 / 剧痛（Pain Crisis） | `pain-crisis-workbench` | `proposed`（未认领、无仓） |
| **CX-012** | 并发症线 | 恶病质 / 营养不良（Cachexia） | `cachexia-workbench` | `proposed`（未认领、无仓） |
| **CX-013** | 并发症线 | 黄疸 / 胆道梗阻（Biliary Obstruction） | `biliary-obstruction-workbench` | `proposed`（未认领、无仓） |
| **生活线** | 生活服务线 | 肿瘤患者生活服务工作台（医保/津贴/基金会/理赔） | `life-service-workbench` | 规划中 · 招募（未建仓） |

### 第二类（建议 1-B）：NCCN T3 / 罕见病 R1 原挂靠未独立建仓项（0 认领 Issue + 0 独立仓）

| 目录编号 | 类型 | 病种名称 | 原挂靠宿主 | 建议独立仓库名 |
| --- | --- | --- | --- | --- |
| **罕见病 #31** | R1 肿瘤型 | 胃肠胰神经内分泌肿瘤（GEP-NET） | `neuroendocrine-workbench` | `gep-net-workbench`（未建仓） |
| **NCCN #16** | NCCN W1 · T3 | 肝胆癌（Hepatobiliary Cancers） | `liver-cancer-workbench` / `biliary-tract-workbench` | `hepatobiliary-workbench`（未建仓） |
| **NCCN #05** | NCCN W0 · T3 | 直肠癌（Rectal Cancer） | `colorectal-workbench` | `rectal-workbench`（未建仓） |
| **NCCN #07** | NCCN W0 · T3 | 小细胞肺癌（SCLC） | 已并入 `lung-cancer-workbench` | 已作为分型并入肺癌仓 |

### 第三类（建议 2-A）：NCCN 主表已认领但远端/本地均未建仓（2 项，可直接补建仓开工）

| 目录编号 | 类型 | 病种名称 | 级别 | 既有 Issue | 建议仓库名 |
| --- | --- | --- | --- | --- | --- |
| **NCCN #22** | NCCN W2 血液肿瘤 | 成人急性淋巴细胞白血病（Adult ALL） | T1 | `#55`（OPEN） | `all-workbench` |
| **NCCN #60** | NCCN W7 儿童肿瘤 | 儿童急性淋巴细胞白血病（Pediatric ALL） | **T0 儿童样板** | `#40`（OPEN） | `pediatric-all-workbench` |

### 第四类（建议 2-B）：13 个 R3 远端 M0–M2 私有孵化仓（非空仓，待接管续建 M3–M7 并装机）

> 领取方式：不新建重复 Issue，直接关联既有 Issue 并 `git clone` 远端仓库，保留既有 G1 草案与原型设计，补齐 `schema/` + `lib/db.mjs` + `dsh/` + `public/` 生产移植 + 双门禁 + Puppeteer 截图墙 + `v0.1.0` 发布与 DSH 装机。

| 罕见病编号 | 病种名称 | 远端仓库（已有 M0–M2） | 既有 Issue | 当前状态 |
| --- | --- | --- | --- | --- |
| **#05** | 阿拉杰里综合征（Alagille） | `alagille-workbench` | `#136` | 待续建 M3–M7 与装机 |
| **#08** | Bardet-Biedl 综合征 | `bbs-workbench` | `#137` | 待续建 M3–M7 与装机 |
| **#11** | CDKL5 缺乏症 | `cdkl5-workbench` | `#143` | 待续建 M3–M7 与装机 |
| **#12** | 无脉络膜症（Choroideremia） | `choroideremia-workbench` | `#131` | 待续建 M3–M7 与装机 |
| **#16** | 先天性胆道闭锁 | `biliary-atresia-workbench` | `#142` | 待续建 M3–M7 与装机 |
| **#21** | 胱氨酸贮积症（Cystinosis） | `cystinosis-workbench` | `#141` | 待续建 M3–M7 与装机 |
| **#27** | 家族性腺瘤性息肉病（FAP） | `fap-workbench` | `#129` | 待续建 M3–M7 与装机 |
| **#29** | 脆性 X 综合征（Fragile X） | `fragile-x-workbench` | `#130` | 待续建 M3–M7 与装机 |
| **#39** | 高林综合征（Gorlin） | `gorlin-workbench` | `#145` | 待续建 M3–M7 与装机 |
| **#41** | 早老症（Progeria / HGPS） | `progeria-workbench` | `#146` | 待续建 M3–M7 与装机 |
| **#43** | Leber 先天性黑矇（LCA） | `lca-workbench` | `#135` | 待续建 M3–M7 与装机 |
| **#71** | 早产儿视网膜病（ROP） | `rop-workbench` | `#147` | 待续建 M3–M7 与装机 |
| **#72** | Rett 综合征 | `rett-workbench` | `#126` | 待续建 M3–M7 与装机 |

---

## 三、近期已完成交付 & 并发在途核验记录

### 本轮已交付发布 `v0.1.0` 并写入 DSH Desktop（已同步 `BACKLOG.md` & `profile/README.md`）
- **NCCN #61 儿童中枢神经系统肿瘤**：`pediatric-cns-workbench` `v0.1.0`（小童脑宝 PedCnsPal · Issue `#161` 已关闭 · 已装机）
- **NCCN #64 儿童霍奇金淋巴瘤**：`pediatric-hodgkin-workbench` `v0.1.0`（小童霍宝 PedHlPal · Issue `#162` 已关闭 · 已装机）
- **NCCN #65 儿童侵袭性成熟 B 细胞淋巴瘤**：`pediatric-b-cell-workbench` `v0.1.0`（小童淋宝 PedBcellPal · Issue `#163` 已关闭 · 已装机）
- **罕见病 #77 腱鞘巨细胞瘤 / PVNS**：`tgct-workbench` `v0.1.0`（小腱宝 TgctPal · Issue `#164` 已关闭 · 已装机）
- **罕见病 #57 骨肉瘤**：`osteosarcoma-workbench` `v0.1.0`（小骨肉宝 OsteoPal · Issue `#171` 已关闭 · 已写入 DSH `package.json`）
- **罕见病 #14 肾透明细胞肉瘤**：`ccsk-workbench` `v0.1.0`（小清肾宝 CcskPal · Issue `#172` 已关闭 · 已写入 DSH `package.json`）

### 并发实例在途（勿重复认领）
- `monogenic-obesity-workbench`（#159）、`pphn-workbench`（#160）、`pghd-workbench`（#157）、`igf1d-workbench`（#158）、`epithelioid-sarcoma-workbench`（#165）、`ppgl-workbench`（#166）、`imt-workbench`（#167）、`gctb-workbench`（#168）、`polycythemia-vera-workbench`（#173）、`myelofibrosis-workbench`（#174）、`CX-005 恶性肠梗阻`（#175）。
