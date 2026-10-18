# 患者工作台开发路线图（Roadmap）

> 本文件是 **xyb-openharness-dsh-plugins** 组织的公开开发目标清单与进度看板。
> 目标池主要参照 **NCCN Guidelines® Treatment by Cancer Type**（2025–2026 版本目录，57+ 类）与国家卫健委等六部门 **《第二批罕见病目录》**（2023 年发布，86 种）。
> 更新日期：2026-10-18。进度以各仓库 `VERSION` 与 `docs/DEV-PLAN.md` 为准，由维护者随迭代更新。

---

## 进度图例

| 图标 | 含义 |
| --- | --- |
| 🟢 | 已发布 / 社区可用 |
| 🔵 | 开发中（有明确里程碑） |
| 🟡 | 设计 / 需求与原型草案阶段 |
| ⚪ | 规划中（已列入排期，未启动） |
| ⬜ | 未启动 · **招募认领中** |

**质量闸口**：每个工作台按 `G1 需求与范围确认 → G2 原型评审 → G3 数据契约冻结 → 实现 → 装机验证` 逐级推进，闸口标准写在各仓库 `docs/` 下。

**立场声明**：所有工作台只提供**信息整理与就诊准备**能力，不做诊断、不做治疗建议、不替代临床判断。

---

## 一、主要癌种工作台

| 癌种 | 品牌 / 代号 | 仓库 | 进度 | 当前状态（2026-10） |
| --- | --- | --- | --- | --- |
| 乳腺癌 | PinkyPal 小粉宝 | [breast-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/breast-cancer-workbench) | 🔵 | v0.5.1；G1/G2/G3 通过；M0 工程底座、M1 数据层、M2 第一段（导入→草稿核对）、MinerU 解析接入已完成；进行中：草稿界面、一图秀真实数据、四点位录入、导出、DSH 接入 |
| 淋巴瘤 | LymBell 小铃铛 | [lymphoma-workbench](https://github.com/xyb-openharness-dsh-plugins/lymphoma-workbench) | 🔵 | v0.2.0；分型整理、疗效回顾与就诊准备工作台开发中 |
| 卵巢癌 | （ ovarian） | [ovarian-workbench](https://github.com/xyb-openharness-dsh-plugins/ovarian-workbench) | 🔵 | v0.1.48；病程资料、治疗历程、指标趋势与医患沟通，快速迭代中 |
| 结直肠癌 | Colopal 小畅宝（占位） | 未建仓 | 🟡 | SPEC 草案 + HTML demo 完成（样板项目）；差异化：分子分型矩阵 + 肠道功能与造口 + CEA |
| 胃癌 | Stompal 小胃宝 | 未建仓 | 🟡 | SPEC 草案；差异化：四标志物（HER2/PD-L1/MSI/CLDN18.2）+ 进食与营养 + 体重 |
| 食管癌 | EsopPal 小咽宝（占位） | 未建仓 | 🟡 | SPEC 草案；差异化：鳞/腺 + 分段 + 吞咽与进食通路 + 体重/白蛋白双序列 |
| 宫颈癌 | CerviPal 小莲宝（占位） | 未建仓 | 🟡 | SPEC 草案；差异化：FIGO 2018 + 性与生育（默认私密）+ 放疗与长期影响 |

### 候选癌种（⬜ 未启动 · 招募认领中）

以下按 NCCN 目录与国内患者规模列出高优先候选，欢迎在 Issues 提案认领：

非小细胞肺癌 · 小细胞肺癌 · 前列腺癌 · 肝细胞癌 · 胰腺腺癌 · 甲状腺癌 · 皮肤黑色素瘤 · 多发性骨髓瘤 · 肾癌 · 膀胱癌 · 头颈癌 · 中枢神经系统癌症 · 子宫肿瘤 · 睾丸癌 · 胆道癌 · 胃肠道间质瘤 · 软组织肉瘤 · 原发不明原发灶 …

> 完整 NCCN 病种与版本对照见文末附录 A。

---

## 二、罕见病方向（长期目标池）

以《第二批罕见病目录》（86 种）为长期池，**全部 ⬜ 未启动 · 欢迎认领**。建议优先从有成熟病友组织、随访资料结构化需求明确的病种做起（如肢端肥大症、特发性肺纤维化类、地中海贫血、神经纤维瘤病等）。注意：目录中的「黑色素瘤」「梅克尔细胞癌」「胃肠胰神经内分泌肿瘤」等同时也是癌种，可与主要癌种工作台合并设计。

<details>
<summary>《第二批罕见病目录》86 项全清单（点击展开）</summary>

| # | 疾病 | # | 疾病 |
| --- | --- | --- | --- |
| 1 | 软骨发育不全 | 44 | Lennox-Gastaut 综合征 |
| 2 | 获得性血友病 | 45 | 角膜缘干细胞缺乏症 |
| 3 | 肢端肥大症 | 46 | 恶性高热 |
| 4 | 成人斯蒂尔病 | 47 | 恶性胸膜间皮瘤 |
| 5 | 阿拉杰里综合征（Alagille） | 48 | 黑色素瘤 |
| 6 | α1-抗胰蛋白酶缺乏症 | 49 | 异染性脑白质营养不良 |
| 7 | ANCA 相关血管炎 | 50 | 单基因非综合征性肥胖 |
| 8 | Bardet-Biedl 综合征 | 51 | 多发性内分泌腺瘤病 |
| 9 | 白塞病/贝赫切特综合征 | 52 | 发作性睡病 |
| 10 | 蓝色橡皮疱样痣 | 53 | 神经母细胞瘤 |
| 11 | CDKL5 缺乏症 | 54 | 神经纤维瘤病 |
| 12 | 无脉络膜症 | 55 | 神经元蜡样脂褐质沉积症 |
| 13 | 慢性炎性脱髓鞘性多发性神经根神经病 | 56 | 神经营养性角膜炎 |
| 14 | 肾透明细胞肉瘤 | 57 | 骨肉瘤 |
| 15 | 冷凝集素病 | 58 | 天疱疮 |
| 16 | 先天性胆道闭锁 | 59 | 新生儿持续肺动脉高压 |
| 17 | 先天性凝血因子Ⅶ缺乏症 | 60 | 嗜铬细胞瘤/副神经节瘤 |
| 18 | NLRP3-相关自身炎症性疾病 | 61 | PIK3CA 相关过度生长综合征 |
| 19 | 梅克尔细胞癌 | 62 | 真性红细胞增多症 |
| 20 | 皮肤T细胞淋巴瘤 | 63 | 原发性胆汁性胆管炎 |
| 21 | 胱氨酸贮积症 | 64 | 原发性生长激素缺乏症 |
| 22 | 隆突性皮肤纤维肉瘤 | 65 | 原发性胰岛素样生长因子-1 缺乏症 |
| 23 | 嗜酸性粒细胞性胃肠炎 | 66 | 原发性免疫缺陷病 |
| 24 | 上皮样肉瘤 | 67 | 原发性骨髓纤维化 |
| 25 | 面肩肱型肌营养不良症 | 68 | 原发性硬化性胆管炎 |
| 26 | 家族性噬血细胞淋巴组织细胞增生症 | 69 | 进行性纤维化性间质性肺疾病 |
| 27 | 家族性腺瘤性息肉病 | 70 | 复发性心包炎 |
| 28 | 进行性骨化性纤维发育不良 | 71 | 早产儿视网膜病 |
| 29 | 脆性X综合征 | 72 | Rett 综合征 |
| 30 | 神经节苷脂贮积症 | 73 | 短肠综合征 |
| 31 | 胃肠胰神经内分泌肿瘤 | 74 | 全身型幼年特发性关节炎 |
| 32 | 胃肠间质瘤 | 75 | 系统性肥大细胞增多症 |
| 33 | 泛发性脓疱型银屑病 | 76 | 大动脉炎 |
| 34 | 遗传性甲状旁腺功能减退症 | 77 | 腱鞘巨细胞瘤/色素沉着绒毛结节性滑膜炎 |
| 35 | 巨细胞动脉炎 | 78 | 地中海贫血（重型） |
| 36 | 骨巨细胞瘤 | 79 | 血栓性血小板减少性紫癜 |
| 37 | 血小板无力症 | 80 | 转甲状腺素蛋白淀粉样变性 |
| 38 | 胶质母细胞瘤 | 81 | 肿瘤坏死因子受体相关周期性综合征 |
| 39 | 高林综合征 | 82 | 肿瘤相关骨软化症 |
| 40 | 化脓性汗腺炎 | 83 | Von Hippel-Lindau 综合征 |
| 41 | 早老症 | 84 | 血管性血友病 3 型 |
| 42 | 炎性肌纤维母细胞瘤 | 85 | 华氏巨球蛋白血症/淋巴浆细胞淋巴瘤 |
| 43 | Leber 先天性黑矇 | 86 | West 综合征/婴儿癫痫痉挛综合征 |

</details>

---

## 三、如何参与（诚邀加入）

无论你是**开发者、临床/研究者、病友组织志愿者、翻译或写作者**，都可以认领一个病种或一个模块：

1. **认领病种**：在本仓库或对应工作台仓库提 Issue，说明病种与你的关联（患者/家属/志愿/专业背景均可）。
2. **需求整理**：从「患者一周的真实生活」出发整理场景（复查、指标、用药、就诊沟通、心理与照护），产出 BRIEF 与 SPEC。
3. **原型评审**：单文件 HTML 原型 → G2 评审通过后进入实现。
4. **实现与验证**：本地优先（本机 SQLite，隐私不出设备），遵循数据契约与文案红线（不做诊断建议、不预言复发、不写治愈率）。
5. **提交 PR**：遵循 [Conventional Commits](https://www.conventionalcommits.org/)，使用仓库内 PR/Issue 模板，至少一名维护者评审后合入。

病种工作台基于统一脚手架（xyb-workbench-starter）创建，工程规范与既有仓库保持一致；每个病种必须有**专属差异化模块**，拒绝换名复用。

---

## 附录 A · NCCN Guidelines® Treatment by Cancer Type 目录参照（2025–2026）

> 仅收录病种名称与公开版本号，用作目标池参照；不复制任何指南临床内容。版本号取自 NCCN 官网公开目录，可能随后续更新变化，以 NCCN 官网为准。

| NCCN 病种 | 中文 | 版本 |
| --- | --- | --- |
| Acute Lymphoblastic Leukemia | 急性淋巴细胞白血病 | 2.2025 |
| Acute Myeloid Leukemia | 急性髓系白血病 | 2.2025 |
| Ampullary Adenocarcinoma | 壶腹部腺癌 | 2.2025 |
| Anal Carcinoma | 肛门癌 | 4.2025 |
| Basal Cell Skin Cancer | 基底细胞皮肤癌 | 2.2025 |
| B-Cell Lymphomas | B 细胞淋巴瘤 | 2.2025 |
| Biliary Tract Cancers | 胆道癌 | 2.2025 |
| Bladder Cancer | 膀胱癌 | 1.2025 |
| Bone Cancer | 骨癌 | 2.2025 |
| Breast Cancer | 乳腺癌 | 4.2025 |
| Castleman Disease | 卡斯尔曼病 | 2.2025 |
| Central Nervous System Cancers | 中枢神经系统癌症 | 1.2025 |
| Cervical Cancer | 宫颈癌 | 4.2025 |
| Chronic Lymphocytic Leukemia/Small Lymphocytic Lymphoma | 慢性淋巴细胞白血病/小淋巴细胞淋巴瘤 | 3.2025 |
| Chronic Myeloid Leukemia | 慢性粒细胞白血病 | 1.2026 |
| Colon Cancer | 结肠癌 | 4.2025 |
| Dermatofibrosarcoma Protuberans | 隆突性皮肤纤维肉瘤 | 1.2025 |
| Esophageal and Esophagogastric Junction Cancers | 食管癌和食管胃连接处癌 | 3.2025 |
| Gastric Cancer | 胃癌 | 2.2025 |
| Gastrointestinal Stromal Tumors | 胃肠道间质瘤 | 1.2025 |
| Gestational Trophoblastic Neoplasia | 妊娠滋养细胞肿瘤 | 3.2025 |
| Hairy Cell Leukemia | 毛细胞白血病 | 1.2025 |
| Head and Neck Cancers | 头颈癌 | 4.2025 |
| Hepatobiliary Cancers | 肝胆癌 | 1.2023 |
| Hepatocellular Carcinoma | 肝细胞癌 | 1.2025 |
| Histiocytic Neoplasms | 组织细胞肿瘤 | 1.2025 |
| Hodgkin Lymphoma | 霍奇金淋巴瘤 | 2.2025 |
| Kaposi Sarcoma | 卡波西肉瘤 | 2.2025 |
| Kidney Cancer | 肾癌 | 1.2026 |
| Melanoma: Cutaneous | 黑色素瘤：皮肤 | 2.2025 |
| Melanoma: Uveal | 黑色素瘤：葡萄膜 | 1.2025 |
| Merkel Cell Carcinoma | 默克尔细胞癌 | 2.2025 |
| Mesothelioma: Peritoneal | 间皮瘤：腹膜 | 2.2025 |
| Mesothelioma: Pleural | 间皮瘤：胸膜 | 2.2025 |
| Multiple Myeloma | 多发性骨髓瘤 | 2.2026 |
| Myelodysplastic Syndromes | 骨髓增生异常综合征 | 2.2025 |
| Myeloid/Lymphoid Neoplasms with Eosinophilia and Tyrosine Kinase Gene Fusions | 伴嗜酸性粒细胞增多和酪氨酸激酶基因融合的髓系/淋巴系肿瘤 | 2.2025 |
| Myeloproliferative Neoplasms | 骨髓增生性肿瘤 | 2.2025 |
| Neuroblastoma | 神经母细胞瘤 | 1.2025 |
| Neuroendocrine and Adrenal Tumors | 神经内分泌和肾上腺肿瘤 | 2.2025 |
| Non-Small Cell Lung Cancer | 非小细胞肺癌 | 7.2025 |
| Occult Primary | 原发不明肿瘤 | 2.2025 |
| Ovarian Cancer/Fallopian Tube Cancer/Primary Peritoneal Cancer | 卵巢癌/输卵管癌/原发性腹膜癌 | 3.2025 |
| Pancreatic Adenocarcinoma | 胰腺腺癌 | 2.2025 |
| Pediatric Acute Lymphoblastic Leukemia | 儿童急性淋巴细胞白血病 | 3.2025 |
| Pediatric Aggressive Mature B-Cell Lymphomas | 儿童侵袭性成熟 B 细胞淋巴瘤 | 2.2025 |
| Pediatric Central Nervous System Cancers | 儿童中枢神经系统癌症 | 2.2025 |
| Pediatric Hodgkin Lymphoma | 儿童霍奇金淋巴瘤 | 2.2025 |
| Penile Cancer | 阴茎癌 | 2.2025 |
| Primary Cutaneous Lymphomas | 原发性皮肤淋巴瘤 | 3.2025 |
| Prostate Cancer | 前列腺癌 | 2.2025 |
| Rectal Cancer | 直肠癌 | 4.2025 |
| Small Bowel Adenocarcinoma | 小肠腺癌 | 3.2025 |
| Small Cell Lung Cancer | 小细胞肺癌 | 1.2026 |
| Soft Tissue Sarcoma | 软组织肉瘤 | 1.2025 |
| Squamous Cell Skin Cancer | 鳞状细胞皮肤癌 | 2.2025 |
| Systemic Light Chain Amyloidosis | 系统性轻链淀粉样变性 | 1.2026 |
| Systemic Mastocytosis | 系统性肥大细胞增多症 | 1.2025 |
| T-Cell Lymphomas | T 细胞淋巴瘤 | 2.2025 |
| Testicular Cancer | 睾丸癌 | 2.2025 |
| Thymomas and Thymic Carcinomas | 胸腺瘤和胸腺癌 | 2.2025 |
| Thyroid Carcinoma | 甲状腺癌 | 1.2025 |
| Uterine Neoplasms | 子宫肿瘤 | 3.2025 |
| Vaginal Cancer | 阴道癌 | 5.2025 |
| Vulvar Cancer | 外阴癌 | 1.2025 |
| Waldenström Macroglobulinemia/Lymphoplasmacytic Lymphoma | 华氏巨球蛋白血症/淋巴浆细胞淋巴瘤 | 1.2026 |
| Wilms Tumor (Nephroblastoma) | 肾母细胞瘤 | 2.2025 |

---

## 免责声明

- 本路线图描述的是**患者信息整理工具**的开发计划，不构成医疗建议；所有工作台输出仅供研究与信息参考，不替代专业医疗诊断与医嘱。
- NCCN® 为美国国家综合癌症网络的注册商标；本组织与 NCCN 无关联，仅引用其公开目录中的病种名称与版本号作为开发范围参照。
- 《第二批罕见病目录》条目引自国家卫生健康委员会等六部门 2023 年 9 月公开发布的目录文件。
