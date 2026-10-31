# 贡献指南 · OpenHarness DSH Plugins

> 状态：组织级贡献入口（v0.1，2026-10-29）。
> 工作台四条贡献路径见 [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md)；开发环境与合同见 [DEVELOPMENT.md](DEVELOPMENT.md)。

---

## 1. 谁可以贡献

不需要写代码也能贡献。我们欢迎：

- **患者/家属**：真实经历访谈、就诊问题清单、试用反馈。
- **社区志愿者/病友组织**：认领病种、组织培训、帮扶建档。
- **临床/研究团队**：字段校对、流程与病种差异化、二次开发。
- **开发者**：工作台、模块、MinerU/OCR/知识库/API 适配。
- **API/能力提供方**：knows、RAG、心理、营养、影像、基因解读等。

许可：本组织推荐/默认 **MIT**；历史仓库以各自 `LICENSE` 为准。

---

## 2. 我们最需要的能力（招募）

### 2.1 MinerU 融合能力

- 目标：让病历 PDF/图片/表格的抽取**更快、更准、更简单**。
- 需要：MinerU 原厂/高手、熟悉版面分析/表格还原/OCR 的开发者。
- 具体：批量解析、表格对齐、跨页结构、扫描件质量、失败重试、额度与隐私。
- 入口：Issue「MinerU 能力」+ 说明你熟悉的文档类型与样例（脱敏）。

### 2.2 其它 OCR 工具与项目（多通道）

- 目标：不只依赖 MinerU，提供多 OCR 通道，按文档类型/质量/隐私/成本选择。
- 要求：统一输出 `{ text, pageRef, tables }`；失败不产候选；用户可切换；不替换 MinerU 的既有链路。
- 入口：Issue「OCR 多通道」+ 适配器提案（附脱敏样例与自测结果）。

#### 场景选型（公开资料口径，接入前用脱敏样例自测）

| 场景 | 推荐 | 核心理由 |
| --- | --- | --- |
| 学术论文、多栏排版、高压缩文档 | **DeepSeek-OCR2** | 视觉因果流保障阅读顺序；Token 压缩效率高（公开口径 5–60×） |
| 商业票据、综合性能、成本敏感 | **GLM-OCR** | 0.9B 参数；API 成本低（公开口径约为传统方案 1/10）；支持 vLLM/Ollama |
| 手机拍照、弯曲扫描、低质量图像 | **PaddleOCR-VL-1.5** | 多边形检测应对物理形变；国产芯片适配较好 |
| 高并发解析、图表转代码、流程图 | **Youtu-Parsing** | 并行解码加速（公开口径 5–22×）；Mermaid 输出可直接进知识管理 |
| CPU 高吞吐、轻量离线 | **Indra OCR** | 18MB ONNX、无需 PyTorch；数字 PDF 直读文本层；行框/版面块/阅读顺序 |

模型均在魔搭开源：

- DeepSeek-OCR2：<https://modelscope.cn/models/deepseek-ai/DeepSeek-OCR-2>
- GLM-OCR：<https://modelscope.cn/models/ZhipuAI/GLM-OCR>
- PaddleOCR-VL-1.5：<https://modelscope.cn/models/PaddlePaddle/PaddleOCR-VL-1.5>
- Youtu-Parsing：<https://modelscope.cn/models/Tencent-YouTu-Research/Youtu-Parsing>
- Indra OCR：`pip install indra-ocr`；公开口径 49 页/秒（CPU）、单页约 230ms、11–17× Tesseract/PaddleOCR、精度 41.3（Paddle 35.8 / Tesseract 19.3）

#### 接入原则

1. **不追求“最大模型”，优先“适合这份文档的小专家模型”**。
2. 同一份脱敏样例跑多通道，比较：阅读顺序、表格行列、单位/日期保留、失败率、耗时/成本。
3. 本地优先：能本机不上传；云端需用户同意并说明发送范围。
4. 许可证/商用条款逐个确认；不随包分发模型权重，除非许可允许。
5. 统一出口：`text/pageRef/tables` → `labparse`/候选；失败不产候选。
6. 用户可切换通道；记录引擎/模型版本，便于回溯。

> 公开口径（5–60×、1/10、5–22×、49 页/秒、41.3 vs 35.8/19.3 等）只作选型线索，不是本组织的验收结论；以真实文档自测为准。
>
> 选型理念：不是更大的模型，而是更符合场景、更贴近人类习惯、更聪明高效的小专家模型。

### 2.3 罕见病/肿瘤社区开发者与运营

- 现状与真实应用有差距：字段、流程、话术、就诊准备细节需要一线经验。
- 需要：病种社区开发者、病友组织运营、患者访谈者。
- 你可以：认领病种、补模块、校对内容、组织培训、带病友试用。
- 入口：[BACKLOG.md](BACKLOG.md) / [PROJECTS.md](PROJECTS.md) + Issue 模板。

### 2.4 开源技术力量与公益 API 提供方

- 目标：通过工作台接入更多**垂直、精细**的场景能力。
- 例子：
  - 心理咨询/情绪支持
  - 营养咨询与食谱
  - 医疗知识库（指南/文献/患者教育）
  - 医学影像服务
  - 基因专业解读（如 KHUB OpenGene）
  - knows API、XYB RAG API
- 要求：来源/时效/适用范围可追溯；用户同意；只作参考，不直接写事实。
- 入口：Issue「能力接入」+ API 文档、配额、隐私边界。

---

## 3. 四条贡献路径

| 路径 | 适合 | 第一步 |
| --- | --- | --- |
| A 认领病种 | 能持续投入的开发者/团队 | 提「病种认领」Issue，填分级判定卡 |
| B 贡献模块 | 想改一个功能/组件 | 提 Issue，说明范围与验收 |
| C 内容与医学核对 | 临床/患者/内容作者 | 提「内容核对」Issue，附来源 |
| D 脚手架贡献 | 想改模板/合同/工具 | 提 Issue，跑 starter 检查 |

详细闸口、DoD、PR 自检见 [CONTRIBUTING-WORKBENCH.md](CONTRIBUTING-WORKBENCH.md)。

---

## 4. 开发流程

1. 读 [DEVELOPMENT.md](DEVELOPMENT.md)、[ARCHITECTURE.md](ARCHITECTURE.md)。
2. Fork / 分支；只改目标仓库，不夹带无关文件。
3. 跑 `npm run check`；UI/安装改动附真机截图/录屏。
4. PR 描述贴自检清单；维护者按 Rubric 评审。
5. 合并后由维护者发版/装市场；PR 合并不等于市场立即可见。

### PR 必填

- 目标用户与场景
- 改了什么、没改什么
- 数据/隐私边界（是否上传、发给谁）
- 测试与真机证据
- 已知限制

---

## 5. 四条不可让步

- 不做诊断、治疗建议、疗效判断。
- 不静默上传患者资料；外部调用必须说明发送内容。
- 未核对候选不进事实层；AI 不直接写库。
- 不把真实患者信息、API Key 写进仓库/Issue/日志/截图。

---

## 6. 评审与验收

- 自动检查：语法、schema、包合同、单测、包内容。
- 人工评审：业务正确性、隐私、可追溯、可维护性。
- 真机验收：配置层 / 列表层 / 界面层三层；只到前两层不算装机通过。
- 安全与合规：外部 API、Token、数据发送范围。

---

## 7. 许可与行为

- 推荐/默认 MIT；提交即表示你同意以目标仓库许可证发布。
- 尊重患者与家属；不消费病痛、不制造焦虑。
- 不发布未脱敏的病历、截图、聊天记录。
- 争议以维护者评审为准；安全问题请私下联系维护者。

---

## 8. 联系

- Issues：<https://github.com/xyb-openharness-dsh-plugins/.github/issues>
- 组织首页：<https://github.com/xyb-openharness-dsh-plugins>
- 官网：<https://www.xiaoyibao.com.cn>
- 社区：<https://info.xiao-x-bao.com.cn>
