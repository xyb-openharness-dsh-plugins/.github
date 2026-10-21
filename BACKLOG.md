# 目标池分层表（Backlog）

> 与 [PROGRAM-PLAN.md](PROGRAM-PLAN.md) 配套使用。本表是**唯一的目标池权威位置**，进度以各仓库 `VERSION` 与 `docs/DEV-PLAN.md` 为准。
> 目标池来源：① NCCN Guidelines® Treatment by Cancer Type 目录（2025–2026，67 个条目）②《86 个罕见病病种诊疗指南（2025 年版）》目录（86 种）。
> 更新日期：2026-10-21。

## 图例

| 状态 | 含义 | | 级别 | 含义 |
| --- | --- | --- | --- | --- |
| 🟢 | 社区可用（V1+V2+V3 三层均通过） | | **T0** | 家族样板，全流程满配 |
| 🔵 | 开发中（闸口已签，实现中） | | **T1** | 标准，三闸口全套 |
| 🟡 | 设计中（G1 已签，G2 未签） | | **T2** | 模板化，G2+G3 双签 |
| ⚪ | 规划中（已排波次，未启动） | | **T3** | 挂靠已有工作台，不建仓 |
| ⬜ | 未启动 · **招募认领中** | | **T4** | 观察池，暂不排期 |

> **"PR 已合并" ≠ 可用。** 只有 V1（检查链）+ V2（Desktop 真加载）+ V3（真机业务闭环）三层都过，才能标 🟢。

---

## 一、主要癌种（67 个 NCCN 条目）

### 1.1 已在推进（W0）

| # | NCCN 病种 | 中文 | NCCN 版本 | 家族 | 级别 | 仓库 | 状态 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Breast Cancer | 乳腺癌 | 4.2025 | 乳腺 | T0 | [breast-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/breast-cancer-workbench) | 🔵 v0.8.0 |
| 2 | B-Cell Lymphomas | B 细胞淋巴瘤 | 2.2025 | 血液 | T0 | [lymphoma-workbench](https://github.com/xyb-openharness-dsh-plugins/lymphoma-workbench) | 🔵 v0.3.0 |
| 3 | Ovarian / Fallopian Tube / Primary Peritoneal Cancer | 卵巢癌/输卵管癌/原发性腹膜癌 | 3.2025 | 妇科 | T0 | [ovarian-workbench](https://github.com/xyb-openharness-dsh-plugins/ovarian-workbench) | 🔵 v0.1.51 |
| 4 | Colon Cancer | 结肠癌 | 4.2025 | 消化 | T0（消化样板） | [colorectal-workbench](https://github.com/xyb-openharness-dsh-plugins/colorectal-workbench) | 🟡 v0.1.0 |
| 5 | Rectal Cancer | 直肠癌 | 2.2025 | 消化 | T3（挂结直肠） | 同上 | 🟡 |
| 6 | Non-Small Cell Lung Cancer | 非小细胞肺癌 | 7.2025 | 胸部 | T0 | [lung-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/lung-cancer-workbench) | 🔵 v0.1.2-rc.16 |
| 7 | Small Cell Lung Cancer | 小细胞肺癌 | 1.2026 | 胸部 | T3（挂肺） | 同上 | 🔵 |
| 8 | Gastric Cancer | 胃癌 | 2.2025 | 消化 | T1 | [gastric-workbench](https://github.com/xyb-openharness-dsh-plugins/gastric-workbench) | 🟡 v0.1.0 |
| 9 | Esophageal and Esophagogastric Junction Cancers | 食管癌和食管胃连接处癌 | 3.2025 | 消化 | T1 | [esophageal-workbench](https://github.com/xyb-openharness-dsh-plugins/esophageal-workbench) | 🟡 v0.1.0 |
| 10 | Cervical Cancer | 宫颈癌 | 4.2025 | 妇科 | T1 | [cervical-workbench](https://github.com/xyb-openharness-dsh-plugins/cervical-workbench) | 🟡 v0.1.0 |
| 11 | Pancreatic Adenocarcinoma | 胰腺腺癌 | 2.2025 | 消化 | T1 | [xyb-workbench](https://github.com/xyb-openharness-dsh-plugins/xyb-workbench)（既有，待迁家族基线） | 🔵 |
| 12 | Hodgkin Lymphoma | 霍奇金淋巴瘤 | 2.2025 | 血液 | T3（挂淋巴瘤） | lymphoma-workbench | ⚪ |
| 13 | T-Cell Lymphomas | T 细胞淋巴瘤 | 2.2025 | 血液 | T3（挂淋巴瘤） | lymphoma-workbench | ⚪ |

> 非 NCCN 病种但已在族内：心理支持线 [xiaoxinbao-workbench](https://github.com/xyb-openharness-dsh-plugins/xiaoxinbao-workbench) / [cancer-psych-support-workbench](https://github.com/xyb-openharness-dsh-plugins/cancer-psych-support-workbench)（🟢 0.3.14），作为**共用支撑模块**被各癌种工作台引用，不占病种名额。

### 1.2 W1 · 消化族收口 + 中国高发补位

| # | NCCN 病种 | 中文 | 版本 | 级别 | 建议仓库 | 状态 |
| --- | --- | --- | --- | --- | --- | --- |
| 14 | Hepatocellular Carcinoma | 肝细胞癌 | 1.2025 | **T0** 消化/肝 | `liver-cancer-workbench` | ⬜ 招募 |
| 15 | Biliary Tract Cancers | 胆道癌 | 2.2025 | T2 | `biliary-tract-workbench` | ⬜ |
| 16 | Hepatobiliary Cancers | 肝胆癌 | 1.2023 | T3（挂肝） | 上 | ⬜ |
| 17 | Small Bowel Adenocarcinoma | 小肠腺癌 | 3.2025 | T2 | `small-bowel-workbench` | ⬜ |
| 18 | Ampullary Adenocarcinoma | 壶腹部腺癌 | 2.2025 | T2 | 挂小肠/胆道 | ⬜ |
| 19 | Anal Carcinoma | 肛门癌 | 4.2025 | T2 | `anal-cancer-workbench` | ⬜ |

### 1.3 W2 · 血液肿瘤家族开荒（13 项，最大一族）

| # | NCCN 病种 | 中文 | 版本 | 级别 | 说明 |
| --- | --- | --- | --- | --- | --- |
| 20 | Chronic Myeloid Leukemia | 慢性粒细胞白血病 | 1.2026 | **T0 血液样板** | 最简、路径最清晰，适合开荒 |
| 21 | Acute Myeloid Leukemia | 急性髓系白血病 | 2.2025 | T1 | |
| 22 | Acute Lymphoblastic Leukemia | 急性淋巴细胞白血病 | 2.2025 | T1 | |
| 23 | Multiple Myeloma | 多发性骨髓瘤 | 2.2026 | T1 | 与罕见病 #85 共用族基线 |
| 24 | Chronic Lymphocytic Leukemia/SLL | 慢性淋巴细胞白血病/小淋巴细胞淋巴瘤 | 3.2025 | T1 | |
| 25 | Myelodysplastic Syndromes | 骨髓增生异常综合征 | 2.2025 | T2 | |
| 26 | Myeloproliferative Neoplasms | 骨髓增生性肿瘤 | 2.2025 | T2 | 罕见病 #62/#67 挂此 |
| 27 | Hairy Cell Leukemia | 毛细胞白血病 | 1.2025 | T2 | |
| 28 | Systemic Mastocytosis | 系统性肥大细胞增多症 | 1.2025 | T2 | = 罕见病 #75 |
| 29 | Castleman Disease | 卡斯尔曼病 | 2.2025 | T2 | |
| 30 | Systemic Light Chain Amyloidosis | 系统性轻链淀粉样变性 | 1.2026 | T3（挂 MM） | |
| 31 | Waldenström Macroglobulinemia/LPL | 华氏巨球蛋白血症 | 1.2026 | T3（挂 B 细胞淋巴瘤） | = 罕见病 #85 |
| 32 | Myeloid/Lymphoid Neoplasms with Eosinophilia and TK Fusions | 伴嗜酸粒细胞增多和 TK 基因融合的髓系/淋巴系肿瘤 | 2.2025 | T4 | 国内资料稀缺，暂观察 |
| 33 | Histiocytic Neoplasms | 组织细胞肿瘤 | 1.2025 | T4 | 同 #32 |

### 1.4 W3 · 泌尿与男性

| # | NCCN 病种 | 中文 | 版本 | 级别 |
| --- | --- | --- | --- | --- |
| 34 | Prostate Cancer | 前列腺癌 | 2.2025 | **T0 泌尿样板** |
| 35 | Bladder Cancer | 膀胱癌 | 1.2025 | T1 |
| 36 | Kidney Cancer | 肾癌 | 1.2026 | T1 |
| 37 | Testicular Cancer | 睾丸癌 | 2.2025 | T2 |
| 38 | Penile Cancer | 阴茎癌 | 2.2025 | T4 |

### 1.5 W4 · 胸部收口 + 皮肤开荒

| # | NCCN 病种 | 中文 | 版本 | 级别 | 备注 |
| --- | --- | --- | --- | --- | --- |
| 39 | Thymomas and Thymic Carcinomas | 胸腺瘤和胸腺癌 | 2.2025 | T1 | |
| 40 | Mesothelioma: Pleural | 间皮瘤：胸膜 | 2.2025 | T1 | = 罕见病 #47 |
| 41 | Mesothelioma: Peritoneal | 间皮瘤：腹膜 | 2.2025 | T2 | |
| 42 | Melanoma: Cutaneous | 黑色素瘤：皮肤 | 2.2025 | **T0 皮肤样板** | = 罕见病 #48 |
| 43 | Melanoma: Uveal | 黑色素瘤：葡萄膜 | 1.2025 | T2 | |
| 44 | Merkel Cell Carcinoma | 默克尔细胞癌 | 2.2025 | T2 | = 罕见病 #19 |
| 45 | Basal Cell Skin Cancer | 基底细胞皮肤癌 | 2.2025 | T2 | |
| 46 | Squamous Cell Skin Cancer | 鳞状细胞皮肤癌 | 2.2025 | T2 | |
| 47 | Kaposi Sarcoma | 卡波西肉瘤 | 2.2025 | T3（挂皮肤） | |
| 48 | Dermatofibrosarcoma Protuberans | 隆突性皮肤纤维肉瘤 | 1.2025 | T3（挂肉瘤） | = 罕见病 #22 |

### 1.6 W5 · 头颈与中枢神经

| # | NCCN 病种 | 中文 | 版本 | 级别 | 备注 |
| --- | --- | --- | --- | --- | --- |
| 49 | Head and Neck Cancers | 头颈癌 | 4.2025 | **T0 头颈样板** | 需覆盖鼻咽癌（中国高发） |
| 50 | Thyroid Carcinoma | 甲状腺癌 | 1.2025 | T1 | 中国高发、随访结构化强 |
| 51 | Central Nervous System Cancers | 中枢神经系统癌症 | 1.2025 | T1 | 罕见病 #38 挂此 |
| 52 | Occult Primary | 原发不明肿瘤 | 2.2025 | T4 | 诊断路径为主，患者侧需求待研究 |

### 1.7 W6 · 骨与软组织 + 妇科收口

| # | NCCN 病种 | 中文 | 版本 | 级别 | 备注 |
| --- | --- | --- | --- | --- | --- |
| 53 | Soft Tissue Sarcoma | 软组织肉瘤 | 1.2025 | **T0 肉瘤样板** | |
| 54 | Bone Cancer | 骨癌 | 2.2025 | T1 | 罕见病 #36/#57 挂此 |
| 55 | Gastrointestinal Stromal Tumors | 胃肠道间质瘤 | 1.2025 | T1 | = 罕见病 #32 |
| 56 | Uterine Neoplasms | 子宫肿瘤 | 3.2025 | T1 | |
| 57 | Gestational Trophoblastic Neoplasia | 妊娠滋养细胞肿瘤 | 3.2025 | T1 | 生育与随访强相关 |
| 58 | Vaginal Cancer | 阴道癌 | 5.2025 | T2 | |
| 59 | Vulvar Cancer | 外阴癌 | 1.2025 | T2 | |

### 1.8 W7 · 儿童线（代记主体 = 家长，独立产品形态）

| # | NCCN 病种 | 中文 | 版本 | 级别 |
| --- | --- | --- | --- | --- |
| 60 | Pediatric Acute Lymphoblastic Leukemia | 儿童急性淋巴细胞白血病 | 3.2025 | **T0 儿童样板** |
| 61 | Pediatric Central Nervous System Cancers | 儿童中枢神经系统癌症 | 2.2025 | T1 |
| 62 | Wilms Tumor (Nephroblastoma) | 肾母细胞瘤 | 2.2025 | T1 |
| 63 | Neuroblastoma | 神经母细胞瘤 | 1.2025 | T1（= 罕见病 #53） |
| 64 | Pediatric Hodgkin Lymphoma | 儿童霍奇金淋巴瘤 | 2.2025 | T2 |
| 65 | Pediatric Aggressive Mature B-Cell Lymphomas | 儿童侵袭性成熟 B 细胞淋巴瘤 | 2.2025 | T2 |

### 1.9 补充条目

| # | NCCN 病种 | 中文 | 版本 | 级别 | 说明 |
| --- | --- | --- | --- | --- | --- |
| 66 | Primary Cutaneous Lymphomas | 原发性皮肤淋巴瘤 | 3.2025 | T3（挂淋巴瘤） | = 罕见病 #20 皮肤 T 细胞淋巴瘤 |
| 67 | Neuroendocrine and Adrenal Tumors | 神经内分泌和肾上腺肿瘤 | 2.2025 | T1（W1） | 罕见病 #31 胃肠胰神经内分泌肿瘤、#60 嗜铬细胞瘤/副神经节瘤 挂此 |

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

### 2.1 R1 肿瘤型 · 挂靠癌种线（20 项，不建仓）

| # | 疾病 | 页 | 挂靠到 | 状态 |
| --- | --- | --- | --- | --- |
| 14 | 肾透明细胞肉瘤 | 76 | 儿童肾肿瘤（Wilms） | ⚪ |
| 19 | 梅克尔细胞癌 | 101 | 皮肤线 | ⚪ |
| 20 | 皮肤 T 细胞淋巴瘤 | 106 | 淋巴瘤 | ⚪ |
| 22 | 隆突性皮肤纤维肉瘤 | 127 | 肉瘤 | ⚪ |
| 24 | 上皮样肉瘤 | 139 | 肉瘤 | ⚪ |
| 31 | 胃肠胰神经内分泌肿瘤 | 173 | 消化 / 神经内分泌 | ⚪ |
| 32 | 胃肠间质瘤 | 180 | 肉瘤（GIST） | ⚪ |
| 36 | 骨巨细胞瘤 | 206 | 骨癌 | ⚪ |
| 38 | 胶质母细胞瘤 | 215 | CNS | ⚪ |
| 42 | 炎性肌纤维母细胞瘤 | 245 | 肉瘤 | ⚪ |
| 47 | 恶性胸膜间皮瘤 | 269 | 胸部 | ⚪ |
| 48 | 黑色素瘤 | 278 | 皮肤线（T0 样板已含） | ⚪ |
| 53 | 神经母细胞瘤 | 303 | 儿童线 | ⚪ |
| 57 | 骨肉瘤 | 341 | 骨癌 | ⚪ |
| 60 | 嗜铬细胞瘤/副神经节瘤 | 356 | 神经内分泌与肾上腺 | ⚪ |
| 62 | 真性红细胞增多症 | 363 | MPN | ⚪ |
| 67 | 原发性骨髓纤维化 | 392 | MPN | ⚪ |
| 75 | 系统性肥大细胞增多症 | 443 | 血液族 | ⚪ |
| 77 | 腱鞘巨细胞瘤/色素沉着绒毛结节性滑膜炎 | 462 | 肉瘤 | ⚪ |
| 85 | 华氏巨球蛋白血症/淋巴浆细胞淋巴瘤 | 505 | B 细胞淋巴瘤 | ⚪ |

### 2.2 R2 非肿瘤慢性病型（34 项，FSHD 形态）

形态：无（或极弱）"治疗历程"模块 → **确诊档案 + 功能与日常 + 并发症筛查 + 医保与资源**。

**首批推荐**（有成熟病友组织、随访结构化需求明确）：肢端肥大症 · 白塞病 · ANCA 相关血管炎 · 进行性纤维化性间质性肺疾病 · 发作性睡病 · 转甲状腺素蛋白淀粉样变性 · 原发性胆汁性胆管炎 · 大动脉炎 · 成人斯蒂尔病 · 获得性血友病

| # | 疾病 | 页 | 级别 | 状态 |
| --- | --- | --- | --- | --- |
| 2 | 获得性血友病 | 5 | T2 | ⬜ |
| 3 | 肢端肥大症 | 12 | **T0 R2 样板** | ⬜ 优先 |
| 4 | 成人斯蒂尔病 | 17 | T1 | ⬜ |
| 6 | α1-抗胰蛋白酶缺乏症 | 27 | T2 | ⬜ |
| 7 | ANCA 相关血管炎 | 33 | T1 | ⬜ 优先 |
| 9 | 白塞病/贝赫切特综合征 | 50 | T1 | ⬜ 优先 |
| 13 | 慢性炎性脱髓鞘性多发性神经根神经病 | 70 | T2 | ⬜ |
| 15 | 冷凝集素病 | 82 | T2 | ⬜ |
| 17 | 先天性凝血因子Ⅶ缺乏症 | 90 | T2 | ⬜ |
| 18 | NLRP3-相关自身炎症性疾病 | 96 | T2 | ⬜ |
| 23 | 嗜酸性粒细胞性胃肠炎 | 134 | T2 | ⬜ |
| 25 | 面肩肱型肌营养不良症（FSHD） | 144 | **T0 罕见病样板** | 🟡 [fshd-workbench](https://github.com/xyb-openharness-dsh-plugins/fshd-workbench) v0.1.1 |
| 26 | 家族性噬血细胞淋巴组织细胞增生症 | 151 | T2 | ⬜ |
| 33 | 泛发性脓疱型银屑病 | 185 | T2 | ⬜ |
| 34 | 遗传性甲状旁腺功能减退症 | 189 | T2 | ⬜ |
| 35 | 巨细胞动脉炎 | 200 | T2 | ⬜ |
| 37 | 血小板无力症 | 210 | T2 | ⬜ |
| 40 | 化脓性汗腺炎 | 229 | T2 | ⬜ |
| 45 | 角膜缘干细胞缺乏症 | 261 | T2 | ⬜ |
| 46 | 恶性高热 | 265 | T2 | ⬜ |
| 52 | 发作性睡病 | 295 | T1 | ⬜ 优先 |
| 56 | 神经营养性角膜炎 | 336 | T2 | ⬜ |
| 58 | 天疱疮 | 346 | T2 | ⬜ |
| 63 | 原发性胆汁性胆管炎 | 371 | T1 | ⬜ 优先 |
| 68 | 原发性硬化性胆管炎 | 401 | T2 | ⬜ |
| 69 | 进行性纤维化性间质性肺疾病 | 408 | T1 | ⬜ 优先 |
| 70 | 复发性心包炎 | 412 | T2 | ⬜ |
| 73 | 短肠综合征 | 428 | T2 | ⬜ |
| 76 | 大动脉炎 | 454 | T1 | ⬜ 优先 |
| 79 | 血栓性血小板减少性紫癜 | 472 | T2 | ⬜ |
| 80 | 转甲状腺素蛋白淀粉样变性 | 478 | T1 | ⬜ 优先 |
| 81 | 肿瘤坏死因子受体相关周期性综合征 | 486 | T2 | ⬜ |
| 82 | 肿瘤相关骨软化症 | 490 | T2 | ⬜ |
| 84 | 血管性血友病 3 型 | 500 | T2 | ⬜ |

### 2.3 R3 儿童 / 遗传型（32 项，代记主体 = 家长）

形态：同一账号内"本人 / 代记"双视角；生长发育类指标需年龄性别分层；隐私与分享默认更严。

**首批推荐**：神经纤维瘤病 · 软骨发育不全 · Rett 综合征 · 地中海贫血（重型）· 原发性免疫缺陷病 · Von Hippel-Lindau 综合征

| # | 疾病 | 页 | 级别 | 状态 |
| --- | --- | --- | --- | --- |
| 1 | 软骨发育不全 | 1 | **T0 R3 样板** | ⬜ 优先 |
| 5 | 阿拉杰里综合征 | 22 | T2 | ⬜ |
| 8 | Bardet-Biedl 综合征 | 40 | T2 | ⬜ |
| 10 | 蓝色橡皮疱样痣 | 57 | T2 | ⬜ |
| 11 | 细胞周期蛋白依赖性激酶样 5 缺乏症（CDKL5） | 60 | T2 | ⬜ |
| 12 | 无脉络膜症 | 63 | T2 | ⬜ |
| 16 | 先天性胆道闭锁 | 87 | T2 | ⬜ |
| 21 | 胱氨酸贮积症 | 122 | T2 | ⬜ |
| 27 | 家族性腺瘤性息肉病 | 155 | T2 | ⬜ |
| 28 | 进行性骨化性纤维发育不良（FOP） | 160 | T2 | ⬜ |
| 29 | 脆性 X 综合征 | 164 | T2 | ⬜ |
| 30 | 神经节苷脂贮积症 | 168 | T2 | ⬜ |
| 39 | 高林综合征 | 224 | T2 | ⬜ |
| 41 | 早老症 | 236 | T2 | ⬜ |
| 43 | Leber 先天性黑矇 | 251 | T2 | ⬜ |
| 44 | Lennox-Gastaut 综合征 | 257 | T2 | ⬜ |
| 49 | 异染性脑白质营养不良 | 283 | T2 | ⬜ |
| 50 | 单基因非综合征性肥胖 | 288 | T2 | ⬜ |
| 51 | 多发性内分泌腺瘤病 | 291 | T2 | ⬜ |
| 54 | 神经纤维瘤病 | 314 | T1 | ⬜ 优先 |
| 55 | 神经元蜡样脂褐质沉积症 | 326 | T2 | ⬜ |
| 59 | 新生儿持续肺动脉高压 | 350 | T2 | ⬜ |
| 61 | PIK3CA 相关过度生长综合征 | 360 | T2 | ⬜ |
| 64 | 原发性生长激素缺乏症 | 374 | T2 | ⬜ |
| 65 | 原发性胰岛素样生长因子-1 缺乏症 | 382 | T2 | ⬜ |
| 66 | 原发性免疫缺陷病 | 385 | T1 | ⬜ 优先 |
| 71 | 早产儿视网膜病 | 417 | T2 | ⬜ |
| 72 | Rett 综合征 | 423 | T2 | ⬜ 优先 |
| 74 | 全身型幼年特发性关节炎 | 436 | T2 | ⬜ |
| 78 | 地中海贫血（重型） | 466 | T1 | ⬜ 优先 |
| 83 | Von Hippel-Lindau 综合征 | 494 | T2 | ⬜ 优先 |
| 86 | West 综合征/婴儿癫痫痉挛综合征 | 509 | T2 | ⬜ |

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
| 当前已启动 | 11 个仓库（含 1 个罕见病 FSHD、1 个跨病种心理支持模块） |

---

## 四、如何认领

1. 在 [Issues](https://github.com/xyb-openharness-dsh-plugins) 用 **「病种认领」** 模板提 Issue，填写分级判定卡（PROGRAM-PLAN §3）。
2. 维护者回复确认级别与波次，并在本表把状态从 ⬜ 改为 ⚪/🟡，同时写上认领人与日期。
3. 按 [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md) 开工。
4. 达到 🟢 后维护者同步 `ROADMAP.md`。

> 无人认领的病种**永久停在 ⬜**，不占用波次资源。宁可目标池停在 ⬜，也不交付半成品。

---

## 免责声明

- 本表描述的是**患者信息整理工具**的开发范围，不构成医疗建议。
- NCCN® 为美国国家综合癌症网络注册商标；本组织与 NCCN 无关联，仅引用其公开目录中的病种名称与版本号。
- 《86 个罕见病病种诊疗指南（2025 年版）》为国家卫生健康委发布的公开文件，本组织仅引用其病种目录与术语作为范围参照，不复制其临床内容。
