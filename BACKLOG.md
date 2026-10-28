# 目标池分层表（Backlog）

> 与 [PROGRAM-PLAN.md](PROGRAM-PLAN.md) 配套使用。本表是**唯一的目标池权威位置**，进度以各仓库 `VERSION` 与 `docs/DEV-PLAN.md` 为准。
> 目标池来源：① NCCN Guidelines® Treatment by Cancer Type 目录（2025–2026，67 个条目）②《86 个罕见病病种诊疗指南（2025 年版）》目录（86 种）。
> 更新日期：2026-10-26。
>
> **想参与但不知道从哪下手 → 直接看 [§〇 优先招募榜](#〇现在最缺人优先招募榜)**：按紧迫度挑了 12 个目标，每项写明"为什么急、缺什么人、第一步能做什么"，附一键认领链接。
> **不知道 ⬜ 到底是缺谁 → 看 [图例 · 招募对象](#招募对象角色代码)**：每个条目的「招募对象」列用角色代码写明缺哪种人，大部分病种最先缺的不是开发。

## 图例

### 进度状态

| 状态 | 含义 |
| --- | --- |
| 🟢 | 社区可用（V1+V2+V3 三层均通过） |
| 🔵 | 开发中（闸口已签，实现中） |
| 🟡 | 设计中（G1 已签，G2 未签） |
| ⚪ | 规划中（已排波次，未启动） |
| ⬜ | **未启动 · 招募认领中**（需要外部贡献者加入，见下节角色说明） |
| 🔥 | **优先招募**（在 §0 榜单内，三维度紧迫度最高的一批） |
| — | 观察池 / 团队在编，暂不对外开放认领 |

> **"PR 已合并" ≠ 可用。** 只有 V1（检查链）+ V2（Desktop 真加载）+ V3（真机业务闭环）三层都过，才能标 🟢。
>
> **⬜ 不等于"缺个程序员"。** 每个 ⬜ 条目后面的「招募对象」列写明了缺的是哪种角色——大部分病种最先缺的不是开发，而是**有真实经历的人**（患者/家属）和**能做医学核对的人**。只有 👤 或 📝 也可以认领，开发可以后配。

### 招募对象（角色代码）

| 代码 | 角色 | 在这个工作台里具体做什么 | 典型投入 |
| --- | --- | --- | --- |
| 👤 | 患者 / 家属 | 提供真实场景与痛点排序：复查节奏、指标困惑、就诊时"不知道该问什么"、副作用日常管理 | 访谈 + 场景清单，几天 |
| 👨‍👩‍👧 | 患儿家长（代记主体） | 同上，但主体是家长视角：长期治疗、异地就医、生长发育与随访、学校与保险 | 访谈 + 场景清单 |
| 🩺 | 临床 / 科研 / 药学 / 护理 | 医学核对：分期与分型术语、指标与参考范围、治疗路径名词、文案红线把关 | 评审式，按次 |
| 💻 | 开发 | 差异化模块实现（脚手架已提供引擎，主要写病种特有的那部分） | 数周 |
| 📝 | 内容 / 医学写作 | 资料整理、就诊问题清单、术语表、患者向解释文案 | 数天～数周 |
| 🤝 | 病友组织 / 社群运营 | 需求征集、用户测试、分发与再招募 | 持续，轻量 |

> 角色可叠加，也可以**只认领其中一个角色**。最低门槛的认领方式是「只做 📝 内容核对」或「只做 👤 场景访谈」——不需要写代码，也不需要一次做完整个病种。

### 为什么先做它：三个维度

分级（T0–T4）只回答"怎么做"，不回答"为什么先做它"。下面是本表排序的真实依据：

| 维度 | 含义 | 取值 |
| --- | --- | --- |
| **规模** | 帮扶人群规模：年新发/存量大体量级 | 十万级 / 万级 / 千级 / 罕见 |
| **信息差** | 患者能拿到的规范信息与实际决策复杂度之间的落差。落差越大，越容易出现"不知道该问什么""被过时信息误导" | 高 / 中 / 低 |
| **危重与时间压力** | 病程进展速度与决策窗口。**生存期越短、决策越不可逆，患者与家属对"把信息理清楚"的需求和压力越大**——他们没有第二次机会慢慢摸索 | 高 / 中 / 低 |

紧迫度 = ★★★（三维度中至少两项"高"）· ★★（一项高）· ★（均未达高）

> 规模与危重度是**定性 + 量级判断**，用于排优先级，不是流行病学统计，也不构成任何预后结论。本表刻意不写具体生存率数字——那类数字一旦脱离分期与个体情况就会被误读；我们只用"决策窗窄 / 慢性病程"这类描述。

---

## 〇、现在最缺人：优先招募榜

> 下面 12 个是**按紧迫度挑出来的**，不是按波次顺序。它们在 §一/§二 里也各自出现，这里集中写清楚"为什么急、缺谁、第一步做什么"。
> 想认领但不确定从哪下手 → 直接从这张表里挑一个。
> ✅ **截至 2026-10-25：榜内 12 项已全部认领。** 进度最快的一批：肝细胞癌（[liver-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/liver-cancer-workbench) 🔵 v0.3.6，G1–G3 已签认）、ATTR（🔵 v0.3.1，真机装机迭代中）、头颈癌（🔵 v0.1.6 已发布，待装机确认）、胶质母细胞瘤 / 胸膜间皮瘤 / 膀胱癌 / 甲状腺癌 / 皮肤黑色素瘤 / 肢端肥大症（G 签认与装机阶段）、肾癌 / GTN（开发版）；儿童急淋（ALL）已认领、建仓待启动（[Issue #40](https://github.com/xyb-openharness-dsh-plugins/.github/issues/40)）。
> **招募重点转向两类：① 已开工工作台的 🩺 医学核对与 👤 患者访谈补位（见「已在推进、但缺人的」表）；② 尚未启动病种的新认领**——W2 其余血液肿瘤、W4 皮肤/胸腺、R2/R3 大部分仍在 ⬜。

### 癌种（9）

| 目标 | 级别 | 规模 | 信息差 | 危重/时间压力 | 缺谁 | 第一步（可只做这一步） | 紧迫度 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **肝细胞癌** ✅ **已认领开工 · 2026-10-24**（[liver-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/liver-cancer-workbench) 🔵 v0.3.6 · 小甘宝 HepPal · G1–G3 已签认，[认领 Issue #10](https://github.com/xyb-openharness-dsh-plugins/.github/issues/10)） | T0 消化/肝样板 · W1 | 十万级（中国高发，乙肝背景为主） | 高：BCLC / CNLC 分期并存，切除·消融·TACE·靶免·移植多路径并行，患者很难自己判断"我属于哪条" | 高：多数确诊已中晚期，肝功能与肿瘤两条线要同时看 | 🩺📝（开发已到位，补内容核对） | 先整理一份「分期与治疗路径名词表 + 确诊后两周要问清的 10 个问题」，不写一行代码也行 | ★★★ |
| **胰腺腺癌**（[认领](https://github.com/xyb-openharness-dsh-plugins/.github/issues/new?template=01-workbench-claim.yml&title=%5B%E8%AE%A4%E9%A2%86%5D%20%E8%83%B0%E8%85%BA%E8%85%BA%E7%99%8C)） | T1 · **已有小胰宝 xyb-workbench v0.1.34**（PDAC 本体，不是待建） | 十万级（发病率仍在上升） | 极高：可切除性判断、新辅助、临床试验、营养与疼痛管理，公众认知普遍停留在"不能手术就没办法" | 极高：病程进展快、决策窗口窄，家属常在数周内做不可逆决定 | 🩺📝💻 | 不是从零建仓：补「不可切除之后」的照护与营养路径，并把既有资料迁到家族基线 | ★★★ |
| **胆道癌**（胆囊/肝内/肝外胆管）✅ **已认领开工 · 2026-10-24**（🟡 v0.1.0 脚手架，本地开发中、远端仓待建；[认领 Issue #18](https://github.com/xyb-openharness-dsh-plugins/.github/issues/18)） | T2 · W1 | 万级 | 极高：分型复杂、患者几乎搜不到成体系的中文规范信息，靠碎片帖子做决策 | 高：生存期短，确诊时常已失去手术机会 | 👤🩺📝 | 最需要的是「有真实经历的人」：先做 3–5 位患者/家属访谈，把场景排出来 | ★★★ |
| **胶质母细胞瘤**（挂 CNS #51 / 罕见病 #38）✅ **已认领开工 · 2026-10-24**（由挂靠升级为独立建仓 [glioblastoma-workbench](https://github.com/xyb-openharness-dsh-plugins/glioblastoma-workbench) 🔵 v0.1.5 · 小星宝 StarPal，[认领 Issue #12](https://github.com/xyb-openharness-dsh-plugins/.github/issues/12)） | T1（已升级为独立建仓） | 万级 | 高：放化疗+电场治疗+复发后选择，信息高度不对称 | 极高：病程短，且认知/人格改变对家属的冲击远超其他瘤种 | 🩺📝👨‍👩‍👧 | 先写「家属视角的时间线」：从确诊到复发，每个节点要准备什么 | ★★★ |
| **前列腺癌** ✅ **已认领开工 · 2026-10-22**（[prostate-workbench](https://github.com/xyb-openharness-dsh-plugins/prostate-workbench) 🟡 v0.1.0 脚手架，[认领 Issue #9](https://github.com/xyb-openharness-dsh-plugins/.github/issues/9)） | T0 泌尿样板 · W3 | 十万级（老年男性高发） | 高：PSA 筛查争议、主动监测 vs 根治/放疗的取舍、内分泌治疗循环与间歇给药，患者很难自己权衡"要不要现在就治" | 低—中：多数病程长、生存期长，压力在长期副作用（尿控、性功能）而非时间 | 👤🩺（最缺访谈） | 泌尿族已开工两仓（前列腺脚手架、膀胱原型），但**患者访谈仍是零**：先做 3–5 位患者访谈，把"确诊后到底在纠结什么"排出来，再定 PSA 随访记录模型 | ★★ |
| **头颈癌** ✅ **已认领开工 · 2026-10-25**（[head-neck-workbench](https://github.com/xyb-openharness-dsh-plugins/head-neck-workbench) 🔵 v0.1.6 **已发布**（`v0.1.0`…`v0.1.6` tag + Release 附 tgz，2026-10-25），M0–M7 完成（**市场投稿材料已备齐，卡在仓库私有**）、0.1.6（按用户手工验收 m09018 改了指标卡背面与一图秀读数）已重装进 profile，但 **DSH Desktop 自 08:05 起未运行**（装机 08:47 晚于退出）→ 界面加载待用户打开 DSH Desktop，可用 `node scripts/verify-desktop-load.mjs` 复核；[认领 Issue #24](https://github.com/xyb-openharness-dsh-plugins/.github/issues/24)） | **T0 头颈样板** · W5 | 高发（鼻咽癌在华南明显集中） | 极高：**原发部位决定一切**（口腔/口咽/喉/下咽/鼻咽/唾液腺），公开信息几乎不讲这一层，患者容易把不同部位的预后与方案混算；HPV 阳性口咽癌与吸烟饮酒相关口腔癌被混成一个「头颈癌」口径 | 高：全喉切除**不可逆**，术前对「没有声音的生活」缺乏准备；放疗后口干/吞咽/骨坏死跟十年以上 | 👤🩺📝（最缺访谈，**失声者的需求在文字互联网里天然缺席**） | 先做 3–5 位患者/家属访谈，把「原发部位 → 功能损失 → 最影响生活的一件事」排出来 | ★★★ |
| **儿童急淋（ALL）** ✅ **已认领 · 2026-10-25**（建仓待启动，[认领 Issue #40](https://github.com/xyb-openharness-dsh-plugins/.github/issues/40)） | T0 儿童样板 · W7 | 万级（儿童白血病中最常见） | 高：2–3 年治疗期、方案阶段多、异地就医普遍、全程靠家长记 | 中高：长期治疗，家庭压力主要在过程与不确定性 | 👨‍👩‍👧🩺💻 | 必须**由家长主导**：先把「家长到底在记什么」这份清单写出来（纸质本/微信群/Excel 都算） | ★★★ |
| **多发性骨髓瘤** ✅ **已认领开工 · 2026-10-25**（[myeloma-workbench](https://github.com/xyb-openharness-dsh-plugins/myeloma-workbench) 🟡 v0.1.0 · 小浆宝 MyeloPal，[认领 Issue #27](https://github.com/xyb-openharness-dsh-plugins/.github/issues/27)） | T1 · W2 | 万级（老年患者为主，存量持续累积） | 高：自体移植 / 维持治疗 / 骨相关事件 / 费用与医保，长期循环复发让人疲于应付 | 中：慢性病程但反复复发 | 👤🩺💻 | 先做「复发—再治疗循环」的记录模型：怎么记才看得出趋势 | ★★ |
| **恶性胸膜间皮瘤**（#40 = 罕见病 #47）✅ **已认领开工 · 2026-10-24**（[mesothelioma-workbench](https://github.com/xyb-openharness-dsh-plugins/mesothelioma-workbench) 🔵 v0.1.4，[认领 Issue #13](https://github.com/xyb-openharness-dsh-plugins/.github/issues/13)） | T1 · W4 | 千级（罕见，但石棉暴露人群有集中聚集） | 极高：职业暴露追溯、工伤与法援信息几乎无处可查 | 高：生存期短 | 👤📝🩺 | 罕见病种最缺的是素材：先做 2–3 例访谈 + 收集可用的援助与法援渠道 | ★★ |

### 罕见病（4）

| 目标 | 线别/级别 | 规模 | 信息差 | 危重/时间压力 | 缺谁 | 第一步（可只做这一步） | 紧迫度 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **转甲状腺素蛋白淀粉样变性（ATTR）** ✅ **已认领 · 2026-10-21 · 🔵 v0.3.1（真机装机迭代中）** | R2 · T1 优先 | 罕见（但**误诊池远大于确诊数**） | 极高：长期被当作心衰 / 周围神经病 / 老年退化处理，确诊常滞后数年；新药出现后诊疗路径剧变，网上信息新旧混杂 | 高：确诊晚意味着已出现不可逆器官损害 | 🩺📝👤 | 医学核对是最关键的一环：先把「哪些信号该怀疑 ATTR」做成人话版清单 | ★★★ |
| **进行性纤维化性间质性肺疾病（PF-ILD）** **已认领 · 2026-10-25 · 🔵 v0.2.0（G1 已签 · V1 通过 · V2/V3 未验）**（[认领](https://github.com/xyb-openharness-dsh-plugins/.github/issues/new?template=01-workbench-claim.yml&title=%5B%E8%AE%A4%E9%A2%86%5D%20%E8%BF%9B%E8%A1%8C%E6%80%A7%E7%BA%A4%E7%BB%B4%E5%8C%96%E6%80%A7%E9%97%B4%E8%B4%A8%E6%80%A7%E8%82%BA%E7%96%BE%E7%97%85)） | R2 · T1 优先 | 万级 | 高：抗纤维化药物、氧疗、肺移植评估的决策节点多且不可逆 | 高：肺功能下降不可逆，错过评估窗口就没机会 | 🩺📝 | 先做「肺功能趋势怎么记 + 移植评估该在什么时间点问」 | ★★★ |
| **重型地中海贫血** ✅ **已认领 · 2026-10-25**（[thalassemia-workbench](https://github.com/xyb-openharness-dsh-plugins/thalassemia-workbench) 空仓占位，待开工；[认领 Issue #34](https://github.com/xyb-openharness-dsh-plugins/.github/issues/34)） | R3 · T1 优先 | 万级（南方省份集中，存量患者规模大） | 高：规律输血 + 去铁治疗是终身管理，费用、医保、生育与遗传咨询信息分散 | 中：长期生存，压力在终身负担与家庭规划 | 👨‍👩‍👧🤝📝 | 病友组织成熟，最容易启动：先征集 10 位家长现有记录方式 | ★★★ |
| **神经纤维瘤病** ✅ **已认领开工 · 2026-10-25**（[neurofibromatosis-workbench](https://github.com/xyb-openharness-dsh-plugins/neurofibromatosis-workbench) 🔵 v0.1.4 · 小纤宝 FibroPal，[认领 Issue #41](https://github.com/xyb-openharness-dsh-plugins/.github/issues/41)） | R3 · T1 优先 | 万级 | 高：多系统受累、终身随访、从皮肤到神经到骨骼，患者不知道该挂哪个科 | 中：终身随访，压力在不确定性与代际遗传 | 👤🤝📝🩺 | 先做「终身随访日历」：不同年龄段该查什么 | ★★ |

### 已在推进、但缺人的（既有仓与新开工仓都在补位）

| 目标 | 现状 | 缺谁 | 补什么 |
| --- | --- | --- | --- |
| 卵巢癌 · [ovarian-workbench](https://github.com/xyb-openharness-dsh-plugins/ovarian-workbench) | 🔵 v0.1.51 | 🩺📝 | 复发—维持治疗循环的内容核对；BRCA/HRD 与 PARP 的术语与问题清单 |
| 胃癌 · [gastric-workbench](https://github.com/xyb-openharness-dsh-plugins/gastric-workbench) | 🟡 v0.1.0 | 👤📝 | 进食与营养的真实场景（术后怎么吃、体重怎么称）；四标志物的人话解释 |
| 食管癌 · [esophageal-workbench](https://github.com/xyb-openharness-dsh-plugins/esophageal-workbench) | 🟡 v0.1.0 | 👤📝 | 吞咽分级的日常记录方式；营养通路（鼻饲/造瘘）照护场景 |
| 肺癌 · [lung-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/lung-cancer-workbench) | 🔵 rc.16 | 📝🩺 | **小细胞肺癌（SCLC）已并入**：病理分型 SCLC/NSCLC 已区分，临床记录断言与试验检索已按 `histology=SCLC` 过滤。继续补的是少见驱动基因内容包 |
| 胰腺癌（PDAC）· [xyb-workbench 小胰宝](https://github.com/xyb-openharness-dsh-plugins/xyb-workbench) | 🔵 v0.1.34 | 🩺📝💻 | 「不可切除之后」的照护与营养路径；既有资料迁到消化族家族基线（历史项目，未走脚手架） |
| 肛管癌 · [anal-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/anal-cancer-workbench)（小萌宝 AnalPal） | 🔵 v0.2.0（2026-10-21 认领，G2 已签、开发版） | 👤📝 | 放化疗副作用（放射性皮炎 / 腹泻 / 骨髓抑制）的日常记录方式；造口与排粪功能的真实场景；G3 数据模型签认 |
| 胃肠间质瘤（GIST）· [gist-workbench](https://github.com/xyb-openharness-dsh-plugins/gist-workbench) | 🟡 v0.1.0（2026-10-21 认领） | 👤🩺 | 靶向线序与剂量变更的患者视角核对；多套危险度体系的人话解释；G3 未签认前不做装机 |
| ATTR 淀粉样变 · [attr-workbench](https://github.com/xyb-openharness-dsh-plugins/attr-workbench) | 🔵 v0.3.1（2026-10-21 认领，真机装机迭代中） | 👤🩺 | 「哪些信号该怀疑 ATTR」的人话清单；心脏 / 神经受累的日常记录方式；H1–H5 五条用户假设待访谈核实 |
| 肝细胞癌 · [liver-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/liver-cancer-workbench)（小甘宝 HepPal） | 🔵 v0.3.6（G1–G3 已签认） | 🩺📝 | BCLC/CNLC 分期与治疗路径名词表核对；「确诊后两周要问清的 10 个问题」人话版 |
| 胶质母细胞瘤 · [glioblastoma-workbench](https://github.com/xyb-openharness-dsh-plugins/glioblastoma-workbench)（小星宝 StarPal） | 🔵 v0.1.5（2026-10-25 装机，V2/V3 用户确认；issue #12） | 🩺📝👨‍👩‍👧 | 家属视角时间线核对；KPS / MRI / 激素记录口径的人话解释 |
| 恶性胸膜间皮瘤 · [mesothelioma-workbench](https://github.com/xyb-openharness-dsh-plugins/mesothelioma-workbench) | 🔵 v0.1.4（2026-10-25 装机，V2/V3 用户确认；issue #13） | 👤📝🩺 | 职业暴露追溯与援助/法援渠道素材；2–3 例患者访谈 |
| 膀胱癌 · [bladder-workbench](https://github.com/xyb-openharness-dsh-plugins/bladder-workbench)（小泉宝 UroPal） | 🔵 v0.1.0（2026-10-24 **G1–G3 均已签认**；M0–M5 完成，M6 装机 45/46，M7–M9 未开始；**尚无写入闭环**，开发版只能读） | 👤🩺 | **写入闭环**（记一笔 → 入库 → 回来看见）；灌注与复查场景访谈；组织学变异型的人话解释 |
| 前列腺癌 · [prostate-workbench](https://github.com/xyb-openharness-dsh-plugins/prostate-workbench) | 🟡 v0.1.0（2026-10-22 认领，脚手架） | 👤🩺 | 3–5 位患者访谈，定 PSA 随访记录模型 |
| 甲状腺癌 · [thyroid-workbench](https://github.com/xyb-openharness-dsh-plugins/thyroid-workbench) | 🔵 v0.2.1（2026-10-25 装机，V2/V3 用户确认；issue #17） | 👤🩺📝 | 随访结构化需求访谈；T1–T7 需求清单医学核对 |
| 子宫内膜癌 · [endometrial-workbench](https://github.com/xyb-openharness-dsh-plugins/endometrial-workbench)（小膜宝 EndoPal） | 🔵 v0.3.2（2026-10-25 认领；issue #28） | 👤🩺📝 | 分子分型与 Lynch 家系语境核对；保育经历者访谈 |
| 多发性骨髓瘤 · [myeloma-workbench](https://github.com/xyb-openharness-dsh-plugins/myeloma-workbench)（小浆宝 MyeloPal） | 🟡 v0.1.0（2026-10-25 认领，M0 快照待续；issue #27） | 👤🩺💻 | M 蛋白与治疗线循环记录模型；骨事件与感染医学核对 |
| 皮肤黑色素瘤 · [melanoma-workbench](https://github.com/xyb-openharness-dsh-plugins/melanoma-workbench)（小痣宝 MolePal · T0 样板） | 🔵 v0.3.1（2026-10-25 装机，V2/V3 用户确认；issue #22） | 👤🩺💻 | 自查档案与肢端语境医学核对；T0 样板功能线评审 |
| 胆道癌 · biliary-tract-workbench（本地脚手架，远端仓待建） | 🟡 v0.1.0（2026-10-24 认领） | 👤🩺📝 | 3–5 位患者/家属访谈，把场景排出来 |
| 肾癌 · [github.com/xyb-openharness-dsh-plugins/kidney-workbench](https://github.com/xyb-openharness-dsh-plugins/kidney-workbench)（小肾宝 RenalPal） | 🔵 v0.3.0（2026-10-25 包级装机，G1 已签、M6 开发版完成；[Issue #20](https://github.com/xyb-openharness-dsh-plugins/.github/issues/20)） | 👤🩺 | 术后随访/晚期治疗访谈；保肾决策与肾功能趋势的医学核对 |
| 慢性粒细胞白血病（CML）· [cml-workbench](https://github.com/xyb-openharness-dsh-plugins/cml-workbench)（小粒宝 GranPal · T0 血液样板） | 🟡 v0.1.0（2026-10-25 认领，[Issue #31](https://github.com/xyb-openharness-dsh-plugins/.github/issues/31)） | 👤🩺 | TKI 线序与随访节奏访谈；血液学/细胞遗传学/分子学三层反应口径核对 |
| 慢性淋巴细胞白血病（CLL/SLL）· [cll-workbench](https://github.com/xyb-openharness-dsh-plugins/cll-workbench)（小淋宝 LymPal） | 🔵 v0.7.0（2026-10-25 认领并连发 v0.2.0→v0.7.0，临床匹配页三 tab 补实；[Issue #45](https://github.com/xyb-openharness-dsh-plugins/.github/issues/45)） | 👤🩺📝 | 「观察等待」阶段的心理与记录场景；治疗指征术语人话化 |
| 神经内分泌肿瘤 · [neuroendocrine-workbench](https://github.com/xyb-openharness-dsh-plugins/neuroendocrine-workbench)（小肽宝） | 🟡 v0.1.0（2026-10-25 认领，[Issue #42](https://github.com/xyb-openharness-dsh-plugins/.github/issues/42)） | 👤🩺📝 | 类癌综合征与激素分泌场景访谈；胃肠胰 NET 分级术语核对 |
| 妊娠滋养细胞肿瘤（GTN）· [gtn-workbench](https://github.com/xyb-openharness-dsh-plugins/gtn-workbench)（小葡宝 GraPal） | 🔵 v0.5.0（2026-10-25 认领，[Issue #38](https://github.com/xyb-openharness-dsh-plugins/.github/issues/38)；hCG 趋势与指标管理已实现） | 👤🩺📝 | 生育保育决策场景访谈；hCG 随访口径医学核对 |
| 原发性胆汁性胆管炎（PBC）· [pbc-workbench](https://github.com/xyb-openharness-dsh-plugins/pbc-workbench)（小管宝 DuctPal） | 🟡 v0.2.7（2026-10-25 认领，包已装 / 2 探针全绿 / 85 test；**G1–G3 待签认、真机未确认**，[回填 Issue #43](https://github.com/xyb-openharness-dsh-plugins/.github/issues/43)） | 👤🩺 | 熊去氧胆酸随访与碱性磷酸酶/胆红素趋势核对；乏力瘙痒场景访谈 |
| PF-ILD · [pf-ild-workbench](https://github.com/xyb-openharness-dsh-plugins/pf-ild-workbench)（小呼宝 BreathPal） | 🔵 v0.2.1（2026-10-25 认领，G1 已签 · V1 通过 · V2/V3 未验） | 🩺📝 | 肺功能（FVC/DLCO）趋势记录口径核对；移植评估时间点清单 |

---

## 一、主要癌种（67 个 NCCN 条目）

### 1.1 已在推进（W0）

| # | NCCN 病种 | 中文 | NCCN 版本 | 家族 | 级别 | 仓库 | 状态 | 招募对象 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Breast Cancer | 乳腺癌 | 4.2025 | 乳腺 | T0 | [breast-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/breast-cancer-workbench) | 🔵 v0.12.0 | 团队在编 |
| 2 | B-Cell Lymphomas | B 细胞淋巴瘤 | 2.2025 | 血液 | T0 | [lymphoma-workbench](https://github.com/xyb-openharness-dsh-plugins/lymphoma-workbench) | 🔵 v0.3.0 | 团队在编 |
| 3 | Ovarian / Fallopian Tube / Primary Peritoneal Cancer | 卵巢癌/输卵管癌/原发性腹膜癌 | 3.2025 | 妇科 | T0 | [ovarian-workbench](https://github.com/xyb-openharness-dsh-plugins/ovarian-workbench) | 🔵 v0.1.51 | 📝🩺 内容补位 |
| 4 | Colon Cancer | 结肠癌 | 4.2025 | 消化 | T0（消化样板） | [colorectal-workbench](https://github.com/xyb-openharness-dsh-plugins/colorectal-workbench) | 🟡 v0.1.0 | 团队在编 |
| 5 | Rectal Cancer | 直肠癌 | 2.2025 | 消化 | T3（挂结直肠） | 同上 | 🟡 | 团队在编 |
| 6 | Non-Small Cell Lung Cancer | 非小细胞肺癌 | 7.2025 | 胸部 | T0 | [lung-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/lung-cancer-workbench) | 🔵 v0.1.2-rc.16 | 团队在编 |
| 7 | Small Cell Lung Cancer | 小细胞肺癌 | 1.2026 | 胸部 | T3（**已并入肺癌工作台**） | 同上 | 🔵 已并入 v0.1.2-rc.16 | 已并入（不单独招募） |
| 8 | Gastric Cancer | 胃癌 | 2.2025 | 消化 | T1 | [gastric-workbench](https://github.com/xyb-openharness-dsh-plugins/gastric-workbench) | 🟡 v0.1.0 | 👤📝 场景/文案 |
| 9 | Esophageal and Esophagogastric Junction Cancers | 食管癌和食管胃连接处癌 | 3.2025 | 消化 | T1 | [esophageal-workbench](https://github.com/xyb-openharness-dsh-plugins/esophageal-workbench) | 🟡 v0.1.0 | 👤📝 场景/文案 |
| 10 | Cervical Cancer | 宫颈癌 | 4.2025 | 妇科 | T1 | [cervical-workbench](https://github.com/xyb-openharness-dsh-plugins/cervical-workbench) | 🟡 v0.1.1 | 团队在编 |
| 68 | Uterine Neoplasms（子宫内膜癌） | 子宫内膜癌 | 待核验 | 妇科 | T1 | [endometrial-workbench](https://github.com/xyb-openharness-dsh-plugins/endometrial-workbench)（2026-10-25 新增条目，FIGO 2023 分子分型整合分期；与 1.7 #56 子宫肿瘤同一仓） | 🔵 v0.3.2（10-25 认领，小膜宝 EndoPal） | 👤🩺📝 补位 |
| 11 | Pancreatic Adenocarcinoma | 胰腺腺癌（PDAC） | 2.2025 | 消化 | T1 | [xyb-workbench](https://github.com/xyb-openharness-dsh-plugins/xyb-workbench) · **小胰宝**（PDAC 本体，非挂靠） | 🔵 v0.1.34 | 🩺📝 内容补位 · 💻 家族基线迁移 |
| 12 | Hodgkin Lymphoma | 霍奇金淋巴瘤 | 2.2025 | 血液 | T3（挂淋巴瘤） | lymphoma-workbench | ⚪ 规划中 | 📝 |
| 13 | T-Cell Lymphomas | T 细胞淋巴瘤 | 2.2025 | 血液 | T3（挂淋巴瘤） | lymphoma-workbench | ⚪ 规划中 | 📝 |

> 非 NCCN 病种但已在族内：心理支持线 [xiaoxinbao-workbench](https://github.com/xyb-openharness-dsh-plugins/xiaoxinbao-workbench)（🟢 0.3.14），作为**共用支撑模块**被各癌种工作台引用，不占病种名额。
> 2026-10-25 跨仓统一动作：各工作台新增「疾病概要」模块（业务顶栏「?」入口 + README 四段式介绍），primer 模板同步自 starter 1.6.1（脚手架已迭代至 1.7.0，补 Windows 装机写法）。

### 1.2 W1 · 消化族收口 + 中国高发补位

| # | NCCN 病种 | 中文 | 版本 | 级别 | 建议仓库 | 状态 | 招募对象 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 14 | Hepatocellular Carcinoma | 肝细胞癌 | 1.2025 | **T0** 消化/肝 | [liver-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/liver-cancer-workbench) | 🔵 v0.3.6（2026-10-24 认领开工，G1–G3 已签认） | 🩺📝 补位 |
| 15 | Biliary Tract Cancers | 胆道癌 | 2.2025 | T2 | biliary-tract-workbench（本地脚手架，远端仓待建） | 🟡 v0.1.0（2026-10-24 认领，[Issue #18](https://github.com/xyb-openharness-dsh-plugins/.github/issues/18)） | 🔥 👤🩺📝 |
| 16 | Hepatobiliary Cancers | 肝胆癌 | 1.2023 | T3（挂肝） | 上 | ⬜ 招募中 | 📝 |
| 17 | Small Bowel Adenocarcinoma | 小肠腺癌 | 3.2025 | T2 | `small-bowel-workbench` | ⬜ 招募中 | 👤📝 |
| 18 | Ampullary Adenocarcinoma | 壶腹部腺癌 | 2.2025 | T2 | 挂小肠/胆道 | ⬜ 招募中 | 📝 |
| 19 | Anal Carcinoma | 肛门癌 | 4.2025 | T2 | [anal-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/anal-cancer-workbench) | 🔵 v0.2.0（2026-10-21 认领，G2 已签） | 👤📝 补位 |

### 1.3 W2 · 血液肿瘤家族开荒（13 项，最大一族）

> #20 慢粒（CML）、#23 多发性骨髓瘤、#24 CLL/SLL 已于 2026-10-25 认领建仓；其余 **⬜ 招募中**。🔥 项在 §0 优先招募榜内有详细理由。

| # | NCCN 病种 | 中文 | 版本 | 级别 | 说明 | 招募对象 |
| --- | --- | --- | --- | --- | --- | --- |
| 20 | Chronic Myeloid Leukemia | 慢性粒细胞白血病 | 1.2026 | **T0 血液样板** · 🟡 [cml-workbench](https://github.com/xyb-openharness-dsh-plugins/cml-workbench) v0.1.0（10-25 认领，小粒宝 GranPal） | 最简、路径最清晰，适合开荒 | 👤🩺 补位 |
| 21 | Acute Myeloid Leukemia | 急性髓系白血病 | 2.2025 | T1 | 🔵 [aml-workbench](https://github.com/xyb-openharness-dsh-plugins/aml-workbench) v0.4.0（2026-10-26 认领开发，[Issue #48](https://github.com/xyb-openharness-dsh-plugins/.github/issues/48)；G1 决策定稿/G2·G3 待签；V1 过+V2 装机，V3 真机待走查；家族首创 dayGrid 按天历 + hourLane 小时轨道；0.4.0 真机反馈轮：临床研究一级菜单按 35 号三步 + 通用写族） | 👤🩺（开发位已满） |
| 22 | Acute Lymphoblastic Leukemia | 急性淋巴细胞白血病 | 2.2025 | T1 | | 👤🩺💻 |
| 23 | Multiple Myeloma | 多发性骨髓瘤 | 2.2026 | T1 · 🟡 [myeloma-workbench](https://github.com/xyb-openharness-dsh-plugins/myeloma-workbench) v0.1.0（10-25 认领，小浆宝 MyeloPal） | 与罕见病 #85 共用族基线 | 👤🩺 补位 |
| 24 | Chronic Lymphocytic Leukemia/SLL | 慢性淋巴细胞白血病/小淋巴细胞淋巴瘤 | 3.2025 | T1 · 🔵 [cll-workbench](https://github.com/xyb-openharness-dsh-plugins/cll-workbench) v0.7.0（10-25 认领，小淋宝 LymPal） | | 👤🩺📝 补位 |
| 25 | Myelodysplastic Syndromes | 骨髓增生异常综合征 | 2.2025 | T2 | | 👤🩺📝 |
| 26 | Myeloproliferative Neoplasms | 骨髓增生性肿瘤 | 2.2025 | T2 | 罕见病 #62/#67 挂此 | 👤🩺📝 |
| 27 | Hairy Cell Leukemia | 毛细胞白血病 | 1.2025 | T2 | | 📝 |
| 28 | Systemic Mastocytosis | 系统性肥大细胞增多症 | 1.2025 | T2 | = 罕见病 #75 | 👤📝 |
| 29 | Castleman Disease | 卡斯尔曼病 | 2.2025 | T2 | | 👤📝 |
| 30 | Systemic Light Chain Amyloidosis | 系统性轻链淀粉样变性 | 1.2026 | T3（挂 MM） | | 📝 |
| 31 | Waldenström Macroglobulinemia/LPL | 华氏巨球蛋白血症 | 1.2026 | T3（挂 B 细胞淋巴瘤） | = 罕见病 #85 | 📝 |
| 32 | Myeloid/Lymphoid Neoplasms with Eosinophilia and TK Fusions | 伴嗜酸粒细胞增多和 TK 基因融合的髓系/淋巴系肿瘤 | 2.2025 | T4 | 国内资料稀缺，暂观察 | — |
| 33 | Histiocytic Neoplasms | 组织细胞肿瘤 | 1.2025 | T4 | 同 #32 | — |

### 1.4 W3 · 泌尿与男性

> #34 前列腺癌、#35 膀胱癌已于 2026-10-22/23 认领开工，#36 肾癌于 2026-10-24 认领开工；其余 **⬜ 招募中**（#38 阴茎癌 T4 观察池除外，暂不招募）。

| # | NCCN 病种 | 中文 | 版本 | 级别 | 招募对象 |
| --- | --- | --- | --- | --- | --- |
| 34 | Prostate Cancer | 前列腺癌 | 2.2025 | **T0 泌尿样板** · 🟡 [prostate-workbench](https://github.com/xyb-openharness-dsh-plugins/prostate-workbench) v0.1.0（10-22 认领，脚手架） | 👤🩺 补位（最缺访谈） |
| 35 | Bladder Cancer | 膀胱癌 | 1.2025 | T1 · 🟡 [bladder-workbench](https://github.com/xyb-openharness-dsh-plugins/bladder-workbench) v0.1.0（10-23 认领，SPEC/原型就绪） | 👤🩺 补位 |
| 36 | Kidney Cancer | 肾癌 | 1.2026 | T1 · 🔵 [kidney-workbench](https://github.com/xyb-openharness-dsh-plugins/kidney-workbench) v0.3.0（2026-10-25 包级装机，G1 已签、M6 开发版完成；[Issue #20](https://github.com/xyb-openharness-dsh-plugins/.github/issues/20)） | 👤🩺 补位（最缺访谈） |
| 37 | Testicular Cancer | 睾丸癌 | 2.2025 | T2 | 👤📝 |
| 38 | Penile Cancer | 阴茎癌 | 2.2025 | T4 | — |

### 1.5 W4 · 胸部收口 + 皮肤开荒

> #40 胸膜间皮瘤（10-24）、#42 皮肤黑色素瘤（10-25，T0 样板）已认领开工；其余 **⬜ 招募中**。

| # | NCCN 病种 | 中文 | 版本 | 级别 | 备注 | 招募对象 |
| --- | --- | --- | --- | --- | --- | --- |
| 39 | Thymomas and Thymic Carcinomas | 胸腺瘤和胸腺癌 | 2.2025 | T1 | | 👤📝🩺 |
| 40 | Mesothelioma: Pleural | 间皮瘤：胸膜 | 2.2025 | T1 · 🔵 [mesothelioma-workbench](https://github.com/xyb-openharness-dsh-plugins/mesothelioma-workbench) v0.1.4（10-24 认领） | = 罕见病 #47 | 👤🩺📝 补位（访谈素材仍最缺） |
| 41 | Mesothelioma: Peritoneal | 间皮瘤：腹膜 | 2.2025 | T2 | | 📝 |
| 42 | Melanoma: Cutaneous | 黑色素瘤：皮肤 | 2.2025 | **T0 皮肤样板** · 🔵 [melanoma-workbench](https://github.com/xyb-openharness-dsh-plugins/melanoma-workbench) v0.3.1（10-25 认领，小痣宝 MolePal，[Issue #22](https://github.com/xyb-openharness-dsh-plugins/.github/issues/22)） | = 罕见病 #48 | 👤🩺 补位 |
| 43 | Melanoma: Uveal | 黑色素瘤：葡萄膜 | 1.2025 | T2 | | 👤📝 |
| 44 | Merkel Cell Carcinoma | 默克尔细胞癌 | 2.2025 | T2 | = 罕见病 #19 | 👤📝 |
| 45 | Basal Cell Skin Cancer | 基底细胞皮肤癌 | 2.2025 | T2 | | 📝 |
| 46 | Squamous Cell Skin Cancer | 鳞状细胞皮肤癌 | 2.2025 | T2 | | 📝 |
| 47 | Kaposi Sarcoma | 卡波西肉瘤 | 2.2025 | T3（挂皮肤） | | 📝 |
| 48 | Dermatofibrosarcoma Protuberans | 隆突性皮肤纤维肉瘤 | 1.2025 | T3（挂肉瘤） | = 罕见病 #22 | 📝 |

### 1.6 W5 · 头颈与中枢神经

> #49 头颈癌于 2026-10-25 认领开工（**T0 头颈样板**）；#50 甲状腺癌已于 2026-10-24 认领开工；#51 CNS 的胶质母细胞瘤已独立建仓（见下行）；其余 **⬜ 招募中**（#52 原发不明 T4 观察池除外）。

| # | NCCN 病种 | 中文 | 版本 | 级别 | 备注 | 招募对象 |
| --- | --- | --- | --- | --- | --- | --- |
| 49 | Head and Neck Cancers | 头颈癌 | 4.2025 | **T0 头颈样板** · 🔵 [head-neck-workbench](https://github.com/xyb-openharness-dsh-plugins/head-neck-workbench) v0.1.6（2026-10-25 认领并发布；G1/G2/G3 已过，10 一级 / 34 二级原型 + 46 表 SQLite + customFrame 外壳；装机产物层已验：34 页签 0 异常、页签差异度审计正文最高 0.227 / 结构最高 0.214（证伪「同一套字段换标题」）、医学断言来源审计 0 硬失败、激活烟测 PASS、重启持久化与 7 组路由 PASS；本机界面加载待用户打开 DSH Desktop（已用 `verify-desktop-load` 把判据固化：运行段切片 / 装机先后 / dshHomePath / state.json / profile 兄弟工作台，含五条反例）；市场条目 YAML + 12 张截图已按 0.1.5 重拍（脚本化，带版本同源断言，修掉了 serve-artifact 写死 0.1.0 导致页面与截图一起显示旧版的问题），**投稿被仓库私有卡住待授权**） | 已覆盖鼻咽癌独立路径（33 二级） | 👤🩺💻 补位 |
| 50 | Thyroid Carcinoma | 甲状腺癌 | 1.2025 | T1 · 🟡 [thyroid-workbench](https://github.com/xyb-openharness-dsh-plugins/thyroid-workbench) v0.1.0（10-24 认领） | 中国高发、随访结构化强 | 👤🩺📝 补位 |
| 51 | Central Nervous System Cancers | 中枢神经系统癌症 | 1.2025 | T1 | 胶质母细胞瘤已独立建仓 [glioblastoma-workbench](https://github.com/xyb-openharness-dsh-plugins/glioblastoma-workbench) 🔵 v0.1.5 小星宝（罕见病 #38 落此仓） | 🩺📝👨‍👩‍👧 补位 |
| 52 | Occult Primary | 原发不明肿瘤 | 2.2025 | T4 | 诊断路径为主，患者侧需求待研究 | — |

### 1.7 W6 · 骨与软组织 + 妇科收口

> GIST（#55，10-21）、软组织肉瘤（#53，10-25，T0 样板）、子宫肿瘤/子宫内膜癌（#56，10-25，与 1.1 #68 条目同仓）、妊娠滋养细胞肿瘤（#57，10-25）已认领开工；其余 **⬜ 招募中**。

| # | NCCN 病种 | 中文 | 版本 | 级别 | 备注 | 状态 | 招募对象 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 53 | Soft Tissue Sarcoma | 软组织肉瘤 | 1.2025 | **T0 肉瘤样板** · 🟡 [sarcoma-workbench](https://github.com/xyb-openharness-dsh-plugins/sarcoma-workbench) v0.1.0（10-25 认领，[Issue #25](https://github.com/xyb-openharness-dsh-plugins/.github/issues/25)） | | 👤🩺 补位 |
| 54 | Bone Cancer | 骨癌 | 2.2025 | T1 | 罕见病 #36/#57 挂此 | ⚪ 规划中 | 👤🩺📝 |
| 55 | Gastrointestinal Stromal Tumors | 胃肠道间质瘤 | 1.2025 | T1 | = 罕见病 #32 · [gist-workbench](https://github.com/xyb-openharness-dsh-plugins/gist-workbench) | 🟡 v0.1.0（2026-10-21 认领） | 👤🩺 补位 |
| 56 | Uterine Neoplasms | 子宫肿瘤 | 3.2025 | T1 · 🔵 [endometrial-workbench](https://github.com/xyb-openharness-dsh-plugins/endometrial-workbench) v0.3.2（10-25 认领，小膜宝 EndoPal；与 1.1 #68 条目同仓） | | 👤🩺📝 补位 |
| 57 | Gestational Trophoblastic Neoplasia | 妊娠滋养细胞肿瘤 | 3.2025 | T1 | 生育与随访强相关 | 🔵 v0.5.0（2026-10-25 认领 issue #38；v0.4.0 走完 M0–M7，v0.5.0 按用户反馈补 12 页菜单/3D 指标卡/营养心理/三档临床匹配/检查与指标二级页签+指标管理；装机层已验 0.5.0，界面加载待用户新建会话确认） | 👤🩺📝 |
| 58 | Vaginal Cancer | 阴道癌 | 5.2025 | T2 | | ⚪ 规划中 | 📝 |
| 59 | Vulvar Cancer | 外阴癌 | 1.2025 | T2 | | ⚪ 规划中 | 📝 |

### 1.8 W7 · 儿童线（代记主体 = 家长，独立产品形态）

> #60 儿童急淋已于 2026-10-25 认领（[Issue #40](https://github.com/xyb-openharness-dsh-plugins/.github/issues/40)，建仓待启动）；其余 **⬜ 招募中**。儿童线的认领主体必须是 👨‍👩‍👧 **患儿家长**——没有家长参与的儿童工作台一律不开工。

| # | NCCN 病种 | 中文 | 版本 | 级别 | 招募对象 |
| --- | --- | --- | --- | --- | --- |
| 60 | Pediatric Acute Lymphoblastic Leukemia | 儿童急性淋巴细胞白血病 | 3.2025 | **T0 儿童样板** · ✅ 已认领（10-25，待建仓） | 👨‍👩‍👧🩺💻 |
| 61 | Pediatric Central Nervous System Cancers | 儿童中枢神经系统癌症 | 2.2025 | T1 | 👨‍👩‍👧🩺💻 |
| 62 | Wilms Tumor (Nephroblastoma) | 肾母细胞瘤 | 2.2025 | T1 | 👨‍👩‍👧🩺📝 |
| 63 | Neuroblastoma | 神经母细胞瘤 | 1.2025 | T1（= 罕见病 #53） | 👨‍👩‍👧🩺📝 |
| 64 | Pediatric Hodgkin Lymphoma | 儿童霍奇金淋巴瘤 | 2.2025 | T2 | 👨‍👩‍👧📝 |
| 65 | Pediatric Aggressive Mature B-Cell Lymphomas | 儿童侵袭性成熟 B 细胞淋巴瘤 | 2.2025 | T2 | 👨‍👩‍👧📝 |

### 1.9 补充条目

> 均为挂靠或跨族条目，需要 📝 内容核对即可启动，不需要建仓。

| # | NCCN 病种 | 中文 | 版本 | 级别 | 说明 | 招募对象 |
| --- | --- | --- | --- | --- | --- | --- |
| 66 | Primary Cutaneous Lymphomas | 原发性皮肤淋巴瘤 | 3.2025 | T3（挂淋巴瘤） | = 罕见病 #20 皮肤 T 细胞淋巴瘤 | 📝 |
| 67 | Neuroendocrine and Adrenal Tumors | 神经内分泌和肾上腺肿瘤 | 2.2025 | T1（W1） · 🟡 [neuroendocrine-workbench](https://github.com/xyb-openharness-dsh-plugins/neuroendocrine-workbench) v0.1.0（10-25 认领，小肽宝） | 罕见病 #31 胃肠胰神经内分泌肿瘤、#60 嗜铬细胞瘤/副神经节瘤 挂此 | 👤🩺📝 补位 |

### 1.10 癌种小计

| 级别 | 数量 | 说明 |
| --- | --- | --- |
| T0 家族样板 | 12 | 乳腺 · B 细胞淋巴瘤 · 卵巢 · 结直肠 · 非小细胞肺癌 · 肝细胞癌 · CML · 皮肤黑色素瘤 · 前列腺 · 头颈 · 软组织肉瘤 · 儿童 ALL |
| T1 标准 | 22 | 三闸口全套，差异化模块 1–2 个 |
| T2 模板化 | 19 | G2+G3 双签，差异配置化 |
| T3 挂靠 | 10 | 不建仓，作为分型/模块进宿主工作台 |
| T4 观察池 | 4 | 暂不排期 |
| **合计** | **67** | **→ 57 个独立建仓单元**（T3 挂靠不建仓） |

> 注：NCCN "Treatment by Cancer Type" 目录实际为 **67 个条目**（含"黑色素瘤：皮肤/葡萄膜"、"间皮瘤：胸膜/腹膜"等分列条目）；坊间流传的"57 种"为旧统计，本表以逐条清点为准。

---

## 二、罕见病（86 种，《86 个罕见病病种诊疗指南（2025 年版）》）

> 页码为该指南目录页，供内容核对时定位；**不复制指南临床内容**，仅作为范围与术语参照。
> 分三条线：**R1 肿瘤型**（挂靠癌种线，不建仓）· **R2 非肿瘤慢性病型**（FSHD 形态）· **R3 儿童/遗传型**（代记主体 = 家长）。

### 2.1 R1 肿瘤型 · 挂靠癌种线（20 项，默认不建仓；#32 GIST、#38 胶质母细胞瘤、#47 胸膜间皮瘤已独立建仓）

| # | 疾病 | 页 | 挂靠到 | 状态 | 招募对象 |
| --- | --- | --- | --- | --- | --- |
| 14 | 肾透明细胞肉瘤 | 76 | 儿童肾肿瘤（Wilms） | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 19 | 梅克尔细胞癌 | 101 | 皮肤线 | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 20 | 皮肤 T 细胞淋巴瘤 | 106 | 淋巴瘤 | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 22 | 隆突性皮肤纤维肉瘤 | 127 | 肉瘤 | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 24 | 上皮样肉瘤 | 139 | 肉瘤 | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 31 | 胃肠胰神经内分泌肿瘤 | 173 | 消化 / 神经内分泌 | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 32 | 胃肠间质瘤 | 180 | [gist-workbench](https://github.com/xyb-openharness-dsh-plugins/gist-workbench)（R1 例外：已独立建仓） | 🟡 v0.1.0（2026-10-21 认领） | 已认领 · 👤🩺 补位 |
| 36 | 骨巨细胞瘤 | 206 | 骨癌 | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 38 | 胶质母细胞瘤 | 215 | [glioblastoma-workbench](https://github.com/xyb-openharness-dsh-plugins/glioblastoma-workbench)（R1 例外：已独立建仓，同 #32 GIST） | 🔵 v0.1.5（2026-10-24 认领） | 已认领 · 🩺📝👨‍👩‍👧 补位 |
| 42 | 炎性肌纤维母细胞瘤 | 245 | 肉瘤 | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 47 | 恶性胸膜间皮瘤 | 269 | 胸部 · [mesothelioma-workbench](https://github.com/xyb-openharness-dsh-plugins/mesothelioma-workbench)（R1 例外：已独立建仓） | 🔵 v0.1.4（2026-10-24 认领） | 已认领 · 👤📝🩺 补位 |
| 48 | 黑色素瘤 | 278 | 皮肤线（T0 样板已含） | ⚪ 规划中 | 已含（皮肤 T0 样板） |
| 53 | 神经母细胞瘤 | 303 | 儿童线 | ⚪ 规划中 | 👨‍👩‍👧🩺📝 |
| 57 | 骨肉瘤 | 341 | 骨癌 | ⚪ 规划中 | 👤🩺📝 |
| 60 | 嗜铬细胞瘤/副神经节瘤 | 356 | 神经内分泌与肾上腺 | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 62 | 真性红细胞增多症 | 363 | MPN | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 67 | 原发性骨髓纤维化 | 392 | MPN | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 75 | 系统性肥大细胞增多症 | 443 | 血液族 | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 77 | 腱鞘巨细胞瘤/色素沉着绒毛结节性滑膜炎 | 462 | 肉瘤 | ⚪ 规划中 | 📝🩺 挂靠内容 |
| 85 | 华氏巨球蛋白血症/淋巴浆细胞淋巴瘤 | 505 | B 细胞淋巴瘤 | ⚪ 规划中 | 📝🩺 挂靠内容 |

### 2.2 R2 非肿瘤慢性病型（34 项，FSHD 形态）

形态：无（或极弱）"治疗历程"模块 → **确诊档案 + 功能与日常 + 并发症筛查 + 医保与资源**。

**首批推荐**（有成熟病友组织、随访结构化需求明确）：肢端肥大症 · 白塞病 · ANCA 相关血管炎 · 进行性纤维化性间质性肺疾病 · 发作性睡病 · 转甲状腺素蛋白淀粉样变性 · 原发性胆汁性胆管炎 · 大动脉炎 · 成人斯蒂尔病 · 获得性血友病

| # | 疾病 | 页 | 级别 | 状态 | 招募对象 |
| --- | --- | --- | --- | --- | --- |
| 2 | 获得性血友病 | 5 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 3 | 肢端肥大症 | 12 | **T0 R2 样板** | 🔵 [acromegaly-workbench](https://github.com/xyb-openharness-dsh-plugins/acromegaly-workbench) v0.2.3（2026-10-25 认领开工，[Issue #30](https://github.com/xyb-openharness-dsh-plugins/.github/issues/30)；G1–G3 签认、V1 过+V2 装机，V3 真机待走查；0.2.1 用户需求：AI 协助一键发送→沉淀 34 号契约入架） | 👤🤝📝🩺（开发位已满） |
| 4 | 成人斯蒂尔病 | 17 | T1 | 🔵 开发中（2026-10-28 认领，[Issue #51](https://github.com/xyb-openharness-dsh-plugins/.github/issues/51)，[aosd-workbench](https://github.com/xyb-openharness-dsh-plugins/aosd-workbench) v0.5.0 开发版已发布；G1 已签、M0–M7 完成，V2/V3 真机待走查） | 👤🤝📝🩺 |
| 6 | α1-抗胰蛋白酶缺乏症 | 27 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 7 | ANCA 相关血管炎 | 33 | T1 | 🟡 [anca-vasculitis-workbench](https://github.com/xyb-openharness-dsh-plugins/anca-vasculitis-workbench) v0.1.0（2026-10-25 认领，小脉宝 VasPal，[Issue #44](https://github.com/xyb-openharness-dsh-plugins/.github/issues/44)） | 👤🤝📝🩺 补位 |
| 9 | 白塞病/贝赫切特综合征 | 50 | T1 | 🔥 优先招募 | 👤🤝📝🩺 |
| 13 | 慢性炎性脱髓鞘性多发性神经根神经病 | 70 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 15 | 冷凝集素病 | 82 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 17 | 先天性凝血因子Ⅶ缺乏症 | 90 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 18 | NLRP3-相关自身炎症性疾病 | 96 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 23 | 嗜酸性粒细胞性胃肠炎 | 134 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 25 | 面肩肱型肌营养不良症（FSHD） | 144 | **T0 罕见病样板** | 🟡 [fshd-workbench](https://github.com/xyb-openharness-dsh-plugins/fshd-workbench) v0.1.1 | 团队在编 |
| 26 | 家族性噬血细胞淋巴组织细胞增生症 | 151 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 33 | 泛发性脓疱型银屑病 | 185 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 34 | 遗传性甲状旁腺功能减退症 | 189 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 35 | 巨细胞动脉炎 | 200 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 37 | 血小板无力症 | 210 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 40 | 化脓性汗腺炎 | 229 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 45 | 角膜缘干细胞缺乏症 | 261 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 46 | 恶性高热 | 265 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 52 | 发作性睡病 | 295 | T1 | ✅ 已认领（2026-10-25，[Issue #37](https://github.com/xyb-openharness-dsh-plugins/.github/issues/37)；[narcolepsy-workbench](https://github.com/xyb-openharness-dsh-plugins/narcolepsy-workbench) 空仓占位，待开工） | 👤🤝📝🩺 |
| 56 | 神经营养性角膜炎 | 336 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 58 | 天疱疮 | 346 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 63 | 原发性胆汁性胆管炎 | 371 | T1 | 🟡 [pbc-workbench](https://github.com/xyb-openharness-dsh-plugins/pbc-workbench) v0.2.7（2026-10-25 认领，小管宝 DuctPal；包已装 / 探针全绿，**G1–G3 待签认、真机未确认**） | 已认领 · 👤🤝📝🩺 |
| 68 | 原发性硬化性胆管炎 | 401 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 69 | 进行性纤维化性间质性肺疾病 | 408 | T1 | 🔵 [pf-ild-workbench](https://github.com/xyb-openharness-dsh-plugins/pf-ild-workbench) v0.2.1（2026-10-25 认领，小呼宝 BreathPal；G1 已签 · V1 通过 · V2/V3 未验） | 🩺📝 补位 |
| 70 | 复发性心包炎 | 412 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 73 | 短肠综合征 | 428 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 76 | 大动脉炎 | 454 | T1 | 🔥 优先招募 | 👤🤝📝🩺 |
| 79 | 血栓性血小板减少性紫癜 | 472 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 80 | 转甲状腺素蛋白淀粉样变性 | 478 | T1 | 🔵 [attr-workbench](https://github.com/xyb-openharness-dsh-plugins/attr-workbench) v0.3.1（2026-10-21 认领，真机装机迭代中） | 已认领 · 👤🩺📝 补位 |
| 81 | 肿瘤坏死因子受体相关周期性综合征 | 486 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 82 | 肿瘤相关骨软化症 | 490 | T2 | ⬜ 招募中 | 👤🤝📝 |
| 84 | 血管性血友病 3 型 | 500 | T2 | ⬜ 招募中 | 👤🤝📝 |

### 2.3 R3 儿童 / 遗传型（32 项，代记主体 = 家长）

形态：同一账号内"本人 / 代记"双视角；生长发育类指标需年龄性别分层；隐私与分享默认更严。

**首批推荐**：神经纤维瘤病 · 软骨发育不全 · Rett 综合征 · 地中海贫血（重型）· 原发性免疫缺陷病 · Von Hippel-Lindau 综合征

| # | 疾病 | 页 | 级别 | 状态 | 招募对象 |
| --- | --- | --- | --- | --- | --- |
| 1 | 软骨发育不全 | 1 | **T0 R3 样板** | 🔥 优先招募 | 👨‍👩‍👧🤝📝🩺💻（R3 样板） |
| 5 | 阿拉杰里综合征 | 22 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 8 | Bardet-Biedl 综合征 | 40 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 10 | 蓝色橡皮疱样痣 | 57 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 11 | 细胞周期蛋白依赖性激酶样 5 缺乏症（CDKL5） | 60 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 12 | 无脉络膜症 | 63 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 16 | 先天性胆道闭锁 | 87 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 21 | 胱氨酸贮积症 | 122 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 27 | 家族性腺瘤性息肉病 | 155 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 28 | 进行性骨化性纤维发育不良（FOP） | 160 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 29 | 脆性 X 综合征 | 164 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 30 | 神经节苷脂贮积症 | 168 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 39 | 高林综合征 | 224 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 41 | 早老症 | 236 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 43 | Leber 先天性黑矇 | 251 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 44 | Lennox-Gastaut 综合征 | 257 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 49 | 异染性脑白质营养不良 | 283 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 50 | 单基因非综合征性肥胖 | 288 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 51 | 多发性内分泌腺瘤病 | 291 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 54 | 神经纤维瘤病 | 314 | T1 | 🔵 [neurofibromatosis-workbench](https://github.com/xyb-openharness-dsh-plugins/neurofibromatosis-workbench) v0.1.4（2026-10-25 认领，小纤宝 FibroPal，[Issue #41](https://github.com/xyb-openharness-dsh-plugins/.github/issues/41)；M0–M7 完成、装机 0.1.4，界面加载待用户新建会话） | 👨‍👩‍👧🤝📝🩺 补位 |
| 55 | 神经元蜡样脂褐质沉积症 | 326 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 59 | 新生儿持续肺动脉高压 | 350 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 61 | PIK3CA 相关过度生长综合征 | 360 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 64 | 原发性生长激素缺乏症 | 374 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 65 | 原发性胰岛素样生长因子-1 缺乏症 | 382 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 66 | 原发性免疫缺陷病 | 385 | T1 | 🔥 优先招募 | 👨‍👩‍👧🤝📝🩺 |
| 71 | 早产儿视网膜病 | 417 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 72 | Rett 综合征 | 423 | T2 | 🔥 优先招募 | 👨‍👩‍👧🤝📝🩺 |
| 74 | 全身型幼年特发性关节炎 | 436 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |
| 78 | 地中海贫血（重型） | 466 | T1 | ✅ 已认领（2026-10-25，[Issue #34](https://github.com/xyb-openharness-dsh-plugins/.github/issues/34)；[thalassemia-workbench](https://github.com/xyb-openharness-dsh-plugins/thalassemia-workbench) 空仓占位，待开工） | 👨‍👩‍👧🤝📝🩺 |
| 83 | Von Hippel-Lindau 综合征 | 494 | T2 | 🔥 优先招募 | 👨‍👩‍👧🤝📝🩺 |
| 86 | West 综合征/婴儿癫痫痉挛综合征 | 509 | T2 | ⬜ 招募中 | 👨‍👩‍👧🤝📝 |

### 2.4 罕见病小计

| 线别 | 数量 | 独立建仓需求 |
| --- | --- | --- |
| R1 肿瘤型（挂靠） | 20 | 0 |
| R2 非肿瘤慢性病型 | 34 | 2 个样板 + 32 个 T1/T2（多数可用同一基线配置化） |
| R3 儿童/遗传型 | 32 | 1 个样板 + 31 个 T2 |
| 合计 | **86** | **3 个样板 + 63 个配置化单元** |

---

## 三、总量

| 口径 | 数量 |
| --- | --- |
| 目标池条目 | **153**（67 个 NCCN 癌种条目 + 86 个罕见病） |
| 去重后需独立设计的单元 | **123**（57 个癌种 + 66 个罕见病；T3 挂靠与 R1 挂靠不建仓） |
| 其中需要走满配 T0 的 | **15**（每个家族 / 每种形态一个样板） |
| 当前已启动 | **38 个工作台**（28 个癌种线 + 9 个罕见病 + 1 个跨病种心理支持）；远端 `*-workbench` 仓 **37 个**（2026-10-25 实查 `gh repo list`，其中发作性睡病、重型地中海贫血 2 个为空仓占位待开工），胆道癌 1 个仅本地脚手架 |
| 计数口径 | 只统计病种/病线工作台；`xfb-workbench`（空占位）与 `find-museum`、`dsh-workbuddy-xdpool` 等站点/工具仓不计入 |

---

## 四、如何认领

### 4.1 三种投入方式（按门槛从高到低）

| 方式 | 适合谁 | 交付物 | 大致投入 | 是否需要建仓 |
| --- | --- | --- | --- | --- |
| **① 整仓认领**（T0 / T1） | 有 👤🩺💻 三类人的小团队，或能长期投入的个人 | 一个完整病种工作台，走完 G1→G2→G3→实现→V1/V2/V3 | 数月 | 是（G1 通过后由维护者建仓） |
| **② 模块认领**（T2 / T3 挂靠） | 单人可完成 | 一个差异化模块或分型模块（如「小细胞肺癌分型包」），进宿主工作台 | 数周 | 否 |
| **③ 内容 / 访谈认领** | **患者、家属、临床、写作者——不需要写代码** | 场景访谈记录、就诊问题清单、术语表、医学核对意见 | 数天 | 否 |

> ③是门槛最低、也最缺的一种方式。**一个病种只要有 3–5 份真实访谈和一份问题清单，就等于把 G1 的一半做完了**——后面开发接手时不必再猜需求。如果你只有两小时，也可以只做一次访谈。

### 4.2 认领流程

1. 在 [Issues](https://github.com/xyb-openharness-dsh-plugins/.github/issues) 用 **「病种认领」** 模板提 Issue（§0 榜单里每项都有**一键认领**直达链接，已预填标题），写清楚：病种、你能投入的角色（👤/🩺/💻/📝/🤝）、投入方式（①②③）、你的关联背景。
2. 维护者回复确认级别、波次与是否建仓，并在本表把状态从 ⬜ 改为 ⚪/🟡，**同时写上认领人、角色与日期**。
3. 按 [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md) 开工。
4. 达到 🟢 后维护者同步 `ROADMAP.md`。

> 想先看看每个项目长什么样？公开侧的 **[PROJECTS.md](PROJECTS.md)** 收录了首批 14 个项目的原型首页截图与能力说明（2026-10-24 前后新开工的 7 个——肝细胞癌、胆道癌、胶质母细胞瘤、间皮瘤、膀胱癌、前列腺癌、甲状腺癌——见各自认领 Issue）；每个已开工项目的对外协作入口就是它自己的认领 Issue（ATTR [#5](https://github.com/xyb-openharness-dsh-plugins/.github/issues/5) · 肛管癌 [#6](https://github.com/xyb-openharness-dsh-plugins/.github/issues/6) · GIST [#7](https://github.com/xyb-openharness-dsh-plugins/.github/issues/7) · 前列腺癌 [#9](https://github.com/xyb-openharness-dsh-plugins/.github/issues/9) · 肝细胞癌 [#10](https://github.com/xyb-openharness-dsh-plugins/.github/issues/10) · 膀胱癌 [#11](https://github.com/xyb-openharness-dsh-plugins/.github/issues/11) · 胶质母细胞瘤 [#12](https://github.com/xyb-openharness-dsh-plugins/.github/issues/12) · 胸膜间皮瘤 [#13](https://github.com/xyb-openharness-dsh-plugins/.github/issues/13) · 甲状腺癌 [#17](https://github.com/xyb-openharness-dsh-plugins/.github/issues/17) · 胆道癌 [#18](https://github.com/xyb-openharness-dsh-plugins/.github/issues/18) · 肾癌 [#20](https://github.com/xyb-openharness-dsh-plugins/.github/issues/20) · 皮肤黑色素瘤 [#22](https://github.com/xyb-openharness-dsh-plugins/.github/issues/22) · 头颈癌 [#24](https://github.com/xyb-openharness-dsh-plugins/.github/issues/24) · 软组织肉瘤 [#25](https://github.com/xyb-openharness-dsh-plugins/.github/issues/25) · 多发性骨髓瘤 [#27](https://github.com/xyb-openharness-dsh-plugins/.github/issues/27) · 子宫内膜癌 [#28](https://github.com/xyb-openharness-dsh-plugins/.github/issues/28) · 肢端肥大症 [#30](https://github.com/xyb-openharness-dsh-plugins/.github/issues/30) · 慢粒 CML [#31](https://github.com/xyb-openharness-dsh-plugins/.github/issues/31) · 重型地中海贫血 [#34](https://github.com/xyb-openharness-dsh-plugins/.github/issues/34) · 原发性胆汁性胆管炎 [#35](https://github.com/xyb-openharness-dsh-plugins/.github/issues/35) · 发作性睡病 [#37](https://github.com/xyb-openharness-dsh-plugins/.github/issues/37) · 妊娠滋养细胞肿瘤 [#38](https://github.com/xyb-openharness-dsh-plugins/.github/issues/38) · 儿童急淋 [#40](https://github.com/xyb-openharness-dsh-plugins/.github/issues/40) · 神经纤维瘤病 [#41](https://github.com/xyb-openharness-dsh-plugins/.github/issues/41) · 神经内分泌 [#42](https://github.com/xyb-openharness-dsh-plugins/.github/issues/42) · ANCA 血管炎 [#44](https://github.com/xyb-openharness-dsh-plugins/.github/issues/44) · CLL/SLL [#45](https://github.com/xyb-openharness-dsh-plugins/.github/issues/45)）。
>
> **认领 ≠ 建仓。** 建仓发生在 G1 通过之后，由维护者执行（见 CONTRIBUTING §10）。在此之前你在自己的 fork 或本地工作即可。
>
> **仓库可见性（2026-10-21 决定）**：病种工作台仓库**一律 private**，新建仓库暂不对外开放；组织内 public 的只有 `.github` 与 `xyb-workbench-starter`。所以本表里的仓库链接**对外部访客会 404，属预期**。外部贡献者在 ① Issue 层认领与评审（不需要权限）→ ② 用可公开的 demo 评审原型 → ③ 需要的写代码的人再逐人最小授权（CONTRIBUTING §10.3）。
>
> 无人认领的病种**永久停在 ⬜**，不占用波次资源。宁可目标池停在 ⬜，也不交付半成品。

---

## 免责声明

- 本表描述的是**患者信息整理工具**的开发范围，不构成医疗建议。
- NCCN® 为美国国家综合癌症网络注册商标；本组织与 NCCN 无关联，仅引用其公开目录中的病种名称与版本号。
- 《86 个罕见病病种诊疗指南（2025 年版）》为国家卫生健康委发布的公开文件，本组织仅引用其病种目录与术语作为范围参照，不复制其临床内容。
