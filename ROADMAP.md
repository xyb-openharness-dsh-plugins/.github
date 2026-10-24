# 患者工作台开发路线图（Roadmap）

> 本文件是 **xyb-openharness-dsh-plugins** 组织的公开开发目标清单与进度看板。
> 目标池主要参照 **NCCN Guidelines® Treatment by Cancer Type**（2025–2026 版本目录，67 个条目）与国家卫生健康委 **《86 个罕见病病种诊疗指南（2025 年版）》**（86 种）。
> 更新日期：2026-10-21。进度以各仓库 `VERSION` 与 `docs/DEV-PLAN.md` 为准，由维护者随迭代更新。
>
> **配套文档（规模化开发）：**
> [PROGRAM-PLAN.md](PROGRAM-PLAN.md) 总纲（分层分级 / 波次 / 七道质量锁）·
> [BACKLOG.md](BACKLOG.md) 153 项目标池分层表、招募对象与认领状态（含 [§〇 优先招募榜](BACKLOG.md#〇现在最缺人优先招募榜)）·
> [PROJECTS.md](PROJECTS.md) 各项目原型首页截图与能力说明（公开侧展示页，链接指向 Issue） ·
> [SCAFFOLD-ITERATION.md](SCAFFOLD-ITERATION.md) 脚手架迭代与经验回流 ·
> [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md) 贡献手册与 PR 流程。

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
153 个目标**不是 153 次全流程**：按 T0 家族样板 / T1 标准 / T2 模板化 / T3 挂靠 / T4 观察池 分级，按波次推进，每波结束留回流窗口。见 [PROGRAM-PLAN.md](PROGRAM-PLAN.md)。

**立场声明**：所有工作台只提供**信息整理与就诊准备**能力，不做诊断、不做治疗建议、不替代临床判断。

---

## 一、主要癌种工作台

| 癌种 | 品牌 / 代号 | 仓库 | 进度 | 当前状态（2026-10） |
| --- | --- | --- | --- | --- |
| 乳腺癌 | PinkyPal 小粉宝 | [breast-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/breast-cancer-workbench) | 🔵 | v0.12.0；G1/G2/G3 已过；M0–M2 第一段与 MinerU 已完成；进行中：草稿界面、一图秀真实数据、四点位录入、导出、DSH 接入 |
| 淋巴瘤 | LymBell 小铃铛 | [lymphoma-workbench](https://github.com/xyb-openharness-dsh-plugins/lymphoma-workbench) | 🔵 | v0.3.0；分型整理、疗效回顾与就诊准备；霍奇金/T 细胞/原发皮肤淋巴瘤拟按 T3 挂靠 |
| 卵巢癌 | Ovarian | [ovarian-workbench](https://github.com/xyb-openharness-dsh-plugins/ovarian-workbench) | 🔵 | v0.1.51；病程资料、治疗历程、指标趋势与医患沟通 |
| 肺癌（NSCLC + SCLC） | 小肺宝 | [lung-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/lung-cancer-workbench) | 🔵 | v0.1.2-rc.15（RC 阶段，未标正式版） |
| 结直肠癌 | Colopal 小畅宝 | [colorectal-workbench](https://github.com/xyb-openharness-dsh-plugins/colorectal-workbench) | 🔵 | **v0.1.0 开发版已推送**（未打 tag / 未发 release）；**消化家族样板**，走通全链路：SPEC → 原型 v0.2 → 2026 资料包 → schema 冻结（G3）→ 开发版 `public/` + `dsh/`；`npm run check` 全绿；待做：DSH Desktop 实机装机验证；差异化：分子分型矩阵 + 肠道功能与造口 + CEA |
| 胃癌 | Stompal 小胃宝 | [gastric-workbench](https://github.com/xyb-openharness-dsh-plugins/gastric-workbench) | 🔵 | **v0.1.0 首个开发版已发布**（tag `v0.1.0`，2026-10-21）；2026 资料包 236 条（119 含中国中心）、22 表 schema 冻结、原型↔开发版 parity 测试全绿；待做：DSH Desktop 实机装机验证；差异化：四标志物（未检测≠阴性）+ 进食与营养（切除方式 / 倾倒 / 补充剂）+ 腹膜与腹腔留痕 |
| 食管癌 | EsopPal 小咽宝 | [esophageal-workbench](https://github.com/xyb-openharness-dsh-plugins/esophageal-workbench) | 🟡 | v0.1.0；鳞/腺 + 分段 + 吞咽与进食通路 + 体重/白蛋白 |
| 宫颈癌 | CerviPal 小莲宝 | [cervical-workbench](https://github.com/xyb-openharness-dsh-plugins/cervical-workbench) | 🟡 | v0.1.1；FIGO 2018 + 性与生育（默认私密）+ 放疗长期影响 |
| 肛管癌 | AnalPal 小萌宝 | [anal-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/anal-cancer-workbench)（对外入口：[Issue #6](https://github.com/xyb-openharness-dsh-plugins/.github/issues/6)） | 🟡 | **2026-10-21 认领开工** · v0.2.0；13 一级页 / 38 二级页原型、19 表 + 1 视图、224 条 2026 临床登记、2 套演示档案；**G1/G2/G3 三道闸口均待签**；差异化：放化疗副作用 + 肠道与排粪功能 + 造口生活 |
| 胃肠间质瘤（GIST） | GistPal 小吉宝 | [gist-workbench](https://github.com/xyb-openharness-dsh-plugins/gist-workbench)（对外入口：[Issue #7](https://github.com/xyb-openharness-dsh-plugins/.github/issues/7)） | 🟡 | **2026-10-21 认领开工** · v0.1.0；阶段 2 已完成（原型↔开发版 parity 10/10）、11 一级页 / 32 二级页、25 表 184 列已冻结、16 条 2026 干预性试验；**G3 未签认，装机未开始**；差异化：病理四事实 + 多套危险度体系 + 靶向线序与剂量变更 + 复查影像结论 |
| 胰腺癌（PDAC） | 小胰宝 | [xyb-workbench](https://github.com/xyb-openharness-dsh-plugins/xyb-workbench) | 🔵 | v0.1.34；历史旗舰项目（未走脚手架），已在本机 Desktop Harness 注册；病程一图秀 / 报告导入解析 / 指标趋势 / 临床试验本地快照 / 营养与心理 / 报告导出；待做：迁到消化族家族基线、补「不可切除之后」照护路径 |
| 肝细胞癌 | 小甘宝 HepPal | [liver-cancer-workbench](https://github.com/xyb-openharness-dsh-plugins/liver-cancer-workbench) | 🟡 | v0.3.2（2026-10-23 开工，G3 已签）；**双轨主脊**：A 肝功能储备 / B 肿瘤负荷并列不加总，门脉高压为第三独立风险线；BCLC 与 CNLC 并存不换算；M5–M7 材料导入链路已闭环。⚠️ 该仓 `VERSION` 与 `package.json` 不同步，待修 |
| 中枢神经系统（胶质母细胞瘤，#51 / 罕见病 #38） | 小星宝 | [glioblastoma-workbench](https://github.com/xyb-openharness-dsh-plugins/glioblastoma-workbench) | 🟡 | v0.1.5（2026-10-24 开工）；CNS 线首个落地，窄宽自适应与宿主接线四要素是这一轮的主要回收 |
| 间皮瘤（胸膜，#40 / 罕见病 #47） | 小胸宝 | [mesothelioma-workbench](https://github.com/xyb-openharness-dsh-plugins/mesothelioma-workbench) | 🟡 | v0.1.0（2026-10-24 开工，G1 已签）；10 线 30 页签已签认，待 G2 |
| 心理支持（跨病种） | 小心宝 | [xiaoxinbao-workbench](https://github.com/xyb-openharness-dsh-plugins/xiaoxinbao-workbench) | 🟢 | v0.3.14；作为**共用支撑模块**被各癌种工作台引用 |

### 下一波（W1）· 消化族收口 + 中国高发补位

~~肝细胞癌~~（🟡 已于 2026-10-23 开工，见上表）· 胆道癌 · 肝胆癌（挂肝）· 小肠腺癌 · 壶腹部腺癌 · ~~肛门癌~~（🟡 已于 2026-10-21 认领，见上表）

### 全部候选与排期

67 个 NCCN 癌种条目 + 86 个罕见病的**完整分级、波次、招募对象与认领状态**见 [BACKLOG.md](BACKLOG.md)，本表不再逐个复制。

**现在最缺人的 12 个**（ATTR 已于 2026-10-21 认领，其余 11 个在招募）（按「帮扶人群规模 · 信息差 · 危重与时间压力」三维挑选，附一键认领链接）：见 [BACKLOG §〇 优先招募榜](BACKLOG.md#〇现在最缺人优先招募榜)。
招募原则：无人认领的病种**永久停在 ⬜**，不占用波次。宁可停在 ⬜，也不交付半成品。
仓库可见性：病种工作台**一律 private**（`.github` 与 `xyb-workbench-starter` 为 public），因此下表仓库链接对外部访客会 404，属预期；外部协作走 Issue 层认领 + demo 层评审 + 逐人代码授权（见 [CONTRIBUTING §10.3](CONTRIBUTING-WORKBENCH.md)）。

---

## 二、罕见病方向（长期目标池）

以《86 个罕见病病种诊疗指南（2025 年版）》的 **86 种**为长期池（完整目录与页码见 [BACKLOG.md](BACKLOG.md)）。**已启动 2 个**（FSHD 形态样板 + ATTR），其余 ⬜ 未启动 · 欢迎认领。
罕见病分三条线，**形态各不相同**，不能当 86 个癌种做：

- **R1 肿瘤型（20 项）**：黑色素瘤、梅克尔细胞癌、GIST、骨肉瘤、神经母细胞瘤、间皮瘤、皮肤 T 细胞淋巴瘤、华氏巨球蛋白血症…… 与癌种重叠 → **T3 挂靠，不重复建仓**。
- **R2 非肿瘤慢性病型（34 项）**：肢端肥大症、白塞病、ANCA 相关血管炎、特发性肺纤维化类、地中海贫血、发作性睡病…… → 参照 FSHD 形态：**确诊档案 + 功能与日常 + 并发症筛查 + 医保与资源**，无（或极弱）"治疗历程"模块。
- **R3 儿童/遗传型（32 项）**：Rett、CDKL5、West 综合征、脆性 X、早老症、软骨发育不全…… → **代记主体 = 家长**，同账号双视角，隐私默认更严。

建议优先从有成熟病友组织、随访结构化需求明确的病种做起。注意：罕见病天然缺指南与 RCT，临床证据模块降级为"登记 + 来源标注"，**不承诺试验匹配**；未核实项一律标注「未核实」，不得用相邻疾病外推。

### 罕见病进行中

| 疾病 | 品牌 / 代号 | 仓库 | 进度 | 当前状态（2026-10） |
| --- | --- | --- | --- | --- |
| 转甲状腺素蛋白淀粉样变性（ATTR，目录 #80） | ATTR-Pal 小甲宝 | [attr-workbench](https://github.com/xyb-openharness-dsh-plugins/attr-workbench) | 🟡 | **2026-10-21 认领开工** · v0.2.0；12 一级页 / 41 页签原型、28 表 schema、434 条临床登记摘录（逐通道终态诚实标注，0 结果 ≠ 无试验）；差异化：型别确认 + 心脏/神经受累双序列 + 治疗耐受（用药记录不评价疗效）+ 家族筛查准备；待做：H1–H5 五条用户假设的访谈核实、ChiCTR / WHO ICTRP 补查；对外入口：[Issue #5](https://github.com/xyb-openharness-dsh-plugins/.github/issues/5) |
| 面肩肱型肌营养不良症（FSHD，目录 #25） | 小飞侠 | [fshd-workbench](https://github.com/xyb-openharness-dsh-plugins/fshd-workbench) | 🟡 | v0.1.1；**罕见病样板**：场景排序已确认，SPEC/SCHEMA 草案 + demo HTML（含右侧 AI pane 状态稿）；差异化：基因确诊档案（D4Z4/4qA）+ 功能与康复（分区+辅助器具）+ 并发症筛查（眼 Coats/听力/呼吸/脊柱）+ 医保与资源；家族内无「治疗历程」模块（无获批治疗药物，聚焦生活/照顾/预防） |

<details>
<summary>《86 个罕见病病种诊疗指南（2025 年版）》— 三条线分组（完整 86 项见 BACKLOG.md）</summary>

- **R1 肿瘤型（挂靠癌种线，20 项）**：#14 肾透明细胞肉瘤 · #19 梅克尔细胞癌 · #20 皮肤 T 细胞淋巴瘤 · #22 隆突性皮肤纤维肉瘤 · #24 上皮样肉瘤 · #31 胃肠胰神经内分泌肿瘤 · #32 胃肠间质瘤（✅ 已独立建仓 gist-workbench）· #36 骨巨细胞瘤 · #38 胶质母细胞瘤 · #42 炎性肌纤维母细胞瘤 · #47 恶性胸膜间皮瘤 · #48 黑色素瘤 · #53 神经母细胞瘤 · #57 骨肉瘤 · #60 嗜铬细胞瘤/副神经节瘤 · #62 真性红细胞增多症 · #67 原发性骨髓纤维化 · #75 系统性肥大细胞增多症 · #77 腱鞘巨细胞瘤 · #85 华氏巨球蛋白血症
- **R2 非肿瘤慢性病型（34 项，首批推荐）**：肢端肥大症 · 白塞病 · ANCA 相关血管炎 · 进行性纤维化性间质性肺疾病 · 发作性睡病 · **转甲状腺素蛋白淀粉样变性（✅ 已认领开工）** · 原发性胆汁性胆管炎 · 大动脉炎 · 成人斯蒂尔病 · 获得性血友病
- **R3 儿童/遗传型（32 项，首批推荐）**：神经纤维瘤病 · 软骨发育不全 · Rett 综合征 · 地中海贫血（重型）· 原发性免疫缺陷病 · Von Hippel-Lindau 综合征

</details>

<details>
<summary>《86 个罕见病病种诊疗指南（2025 年版）》86 项全清单（点击展开）</summary>

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
| 25 | 面肩肱型肌营养不良症 🔵已认领 | 68 | 原发性硬化性胆管炎 |
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

完整流程见 [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md)，四条贡献路径：

| 路径 | 适合谁 | 入口 |
| --- | --- | --- |
| **A 病种认领者** | 患者/家属/临床/志愿者/开发者，愿陪一个病种走完 | 用「病种认领」Issue 模板，填分级判定卡 + 差异化矩阵草案 |
| **B 模块贡献者** | 开发者 | 该病种 G3 已签后，按 `feat/fix/docs` 分支提 PR |
| **C 内容与医学核对者** | 临床、病友组织、医学编辑（无需写代码） | 用「内容与医学核对」Issue 模板：指标字典 / 术语 / 患者解释 / 指南版本 |
| **D 脚手架贡献者** | 有 ≥1 个病种实战经验的开发者 | 用「脚手架反馈」Issue；需满足双病种复现（见 SCAFFOLD-ITERATION） |

无论你是**开发者、临床/研究者、病友组织志愿者、翻译或写作者**，都可以认领一个病种或一个模块：

1. **认领病种**：用 Issue 模板，说明病种与你的关联（患者/家属/志愿/专业背景均可）；维护者回复级别与波次。
2. **需求整理**：从「患者一周的真实生活」出发整理场景，产出 BRIEF 与 SPEC；**差异化矩阵 ≥3 条是准入门槛**。
3. **原型评审**：单文件 HTML 原型 → G2 评审通过后进入实现（未确认不写业务代码）。
4. **实现与验证**：本地优先（本机 SQLite，隐私不出设备），遵循数据契约与文案红线；V1 检查链 + V2 装机 + V3 业务，**三层缺一不算通过**。
5. **提交 PR**：遵循 [Conventional Commits](https://www.conventionalcommits.org/)，使用仓库内 PR/Issue 模板，至少一名维护者评审后合入。

病种工作台基于统一脚手架（xyb-workbench-starter）创建，工程规范与既有仓库保持一致；每个病种必须有**专属差异化模块**，拒绝换名复用。
波次结束有 1–2 周**回流窗口**，把本波经验沉淀进脚手架并发 tag（见 [SCAFFOLD-ITERATION.md](SCAFFOLD-ITERATION.md)）。

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
- 《86 个罕见病病种诊疗指南（2025 年版）》为国家卫生健康委发布的公开文件；本组织仅引用其病种目录与术语作为开发范围参照，**不复制其临床内容**。
