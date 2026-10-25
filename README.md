# 《开放逻辑文本》完整大陆简体中文版（722/722 单元合订读本）

Open Logic Project — Complete Mainland Simplified-Chinese Edition (`zh-Hans-CN`)

## 直接阅读

- [单卷 PDF：868 页，722/722 个来源单元](https://github.com/KokunoYumeto/open-logic-zh-hans-cn/releases/download/ZH-OLP-PUB-0006/OpenLogic_zh-Hans-CN_Standalone722.pdf)
- [英文术语括注对照表：923 处，按页码排列](https://github.com/KokunoYumeto/open-logic-zh-hans-cn/releases/download/ZH-OLP-PUB-0006/OpenLogic_zh-Hans-CN_English_Glosses.tsv)
- [GitHub 项目与可编辑来源](https://github.com/KokunoYumeto/open-logic-zh-hans-cn)

这是 Open Logic Project《开放逻辑文本》的大陆简体中文（`zh-Hans-CN`）学术翻译版。内容涵盖集合、关系与函数、命题逻辑和一阶逻辑、证明系统、模型论、可计算性与不完备性、模态逻辑、证明论、相继式演算、切割消去、自然演绎、正规化、命题即类型及其他专题。

冻结来源为 Open Logic Project 提交 `9620cc73f9c8e0ad003c514a5d3748f29611c4c0` 的全部 722 个内容 TeX 单元。上游完整版驱动程序选用的 642 个单元构成主读本，其余 80 个替代、草稿或实验性单元构成补充读本。两册无删节合订为一份 868 页 PDF：第 1–744 页为主读本，第 745–868 页为补充读本。

## 英文术语括注

术语在正文中首次出现时（不计公式、标题、定理名、图表说明和交叉引用），中文术语后用括注给出英文原词，例如“集合（set）”“非直谓的（impredicative）”“可列（denumerable）集合”。全书共 923 处：主读本 844 处，补充读本 79 处，每处只出现一次。英文一般用小写，专名和缩写除外（如 Kőnig’s lemma、BHK interpretation）。对照表按 PDF 页码列出每一处的中文术语、英文、所在部分和来源文件。

除这些括注外，英文只保留于原书书名、专名、文献条目、代码、公式和稳定标识，不构成并排英文版。

## 阅读版式与导航

正文为宋体五号基准（10.5 pt），行距 15.5 pt，版心居中；主读本与补充读本采用相同的字号、行距和页边距。全部 868 页均为 US Letter（612 × 792 pt）。

合订不重排已排好的页面：868 页的内容流逐页与两份输入 PDF 一致。书签面板分为“主读本（642 个核心单元）”与“补充读本（80 个附加单元）”两大入口。两册有 201 个相同的内部目标名称，因此补充读本的 207 个内部链接在合订时改为明确页目标。全书 3,145 个链接中，内部链接的目标均存在，所有链接矩形都在页面以内。

## 来源、许可与版本边界

原作与作者：Open Logic Project。许可：Creative Commons Attribution 4.0（CC BY 4.0）。本译本保留来源、署名、原作者标注的草稿或未完成状态以及版本改动说明；它不是 Open Logic Project 官方中文版，也不表示原作者或相关机构认可。

中文翻译、英文术语括注与排版均为 AI 生成，尚未经人工中文审校，不声称同行评审、数学或语言认证。

## 文件与重建

发行版 [ZH-OLP-PUB-0006](https://github.com/KokunoYumeto/open-logic-zh-hans-cn/releases/tag/ZH-OLP-PUB-0006) 包含：

- `OpenLogic_zh-Hans-CN_Standalone722.pdf`：单卷阅读器，868 页，722/722 单元。
- `OpenLogic_zh-Hans-CN_English_Glosses.tsv`：英文术语括注对照表（PDF 页、中文术语、英文、所在部分、来源文件；来源文件路径以主读本来源包为准）。
- `OpenLogic_zh-Hans-CN_Source.zip` 与 `OpenLogic_zh-Hans-CN_Supplement80_Source.zip`：主读本和补充读本的可编辑来源。
- `OpenLogic_zh-Hans-CN_Standalone722_Evidence.zip`：构建记录、日志检查、补充读本机械检查、合订脚本及其收据、括注检查和目视检查页。
- `README_Standalone722.md`：本说明。
- `Standalone722_SHA256SUMS.txt`：各发行资产的 SHA-256 与字节数。

重建步骤见 [`BUILD.md`](BUILD.md)，检查结果见 [`evidence/qa.md`](evidence/qa.md)。较早的版本及其翻译生产证据保存在较早的 GitHub 发行版和 [Zenodo 记录](https://doi.org/10.5281/zenodo.21987817)（收录至 2026 年 9 月 5 日的版本）中。

## 已知限制

PDF 未标记结构标签；67 个字体条目中有 5 个数学字体条目缺少 ToUnicode（CMSY10 两个、CMEX10、stmary10、txsyc），因此本版不声称符合 PDF/UA，也不保证全部公式的复制、检索、抽取或屏幕阅读器语义。中文正文所用字体均嵌入且带 ToUnicode。
