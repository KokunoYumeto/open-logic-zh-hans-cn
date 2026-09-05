# 《开放逻辑文本》完整大陆简体中文版（722/722 单元合订读本）

Open Logic Project — Complete Mainland Simplified-Chinese Edition (`zh-Hans-CN`)

## 直接阅读

- [单卷 PDF：859 页，722/722 个来源单元](https://github.com/KokunoYumeto/open-logic-zh-hans-cn/releases/download/ZH-OLP-PUB-0005/OpenLogic_zh-Hans-CN_Standalone722.pdf)
- [Zenodo 概念 DOI：始终指向最新版](https://doi.org/10.5281/zenodo.21987817)
- [GitHub 项目与可编辑来源](https://github.com/KokunoYumeto/open-logic-zh-hans-cn)

这是 Open Logic Project《开放逻辑文本》的大陆简体中文（`zh-Hans-CN`）学术翻译版。内容涵盖集合、关系与函数、命题逻辑和一阶逻辑、证明系统、模型论、可计算性与不完备性、模态逻辑、证明论、相继式演算、切割消去、自然演绎、正规化、命题即类型及其他专题。

冻结来源为 Open Logic Project 提交 `9620cc73f9c8e0ad003c514a5d3748f29611c4c0` 的全部 722 个内容 TeX 单元。此前公开交付把 642 个常规驱动单元排为主读本，把其余 80 个替代、草稿或实验性单元排为补充读本；译文来源已经是 722/722，但没有一份同时包含两部分的单卷阅读器。本版将两册无删节合订为一份 859 页 PDF：第 1–736 页为主读本，第 737–859 页为补充读本，因此阅读器覆盖也达到 722/722。

## 阅读版式与导航

主读本沿用已完成的中文重排：正文为宋体五号基准（10.5 pt），行距 15.5 pt，版心居中为 491 pt × 682 pt，左右边距均为 61.43 pt。补充读本采用相同的 10.5 pt 宋体和 15.5 pt 行距及居中页边距。该配置按大陆数学和科学出版中常见的五号正文尺度处理，避免早期版本正文过小、版心过窄和单双页横向漂移。

合订过程不重排或改写已经冻结的页面内容。机械验证确认 859 页的内容流逐页与两份输入 PDF 完全一致；全部页面均为 US Letter（612 × 792 pt）。书签面板分为“主读本（642 个核心单元）”与“补充读本（80 个附加单元）”两大入口。为避免两册共有的 200 个内部目标名称造成错跳，补充册的 207 个内部链接在合订时改写为明确页目标；最终 3,136 个链接全部保留、均可解析且没有越出页面边界。

## 来源、许可与版本边界

原作与作者：Open Logic Project。许可：Creative Commons Attribution 4.0（CC BY 4.0）。本译本保留来源、署名、原作者标注的草稿或未完成状态以及版本改动说明；它不是 Open Logic Project 官方中文版，也不表示原作者或相关机构认可。

中文翻译与排版为 AI 生成，尚未经人工中文审校，不声称同行评审、数学或语言认证。英文只保留于原书书名、专名、文献条目、代码、公式和稳定标识，不构成并排英文版。

## 文件与重建

- `OpenLogic_zh-Hans-CN_Standalone722.pdf`：本次首要阅读文件，859 页，722/722 单元。
- `OpenLogic_zh-Hans-CN_Source.zip` 与 `OpenLogic_zh-Hans-CN_Supplement80_Source.zip`：主读本和补充读本的可编辑来源。
- `OpenLogic_zh-Hans-CN_Standalone722_Evidence.zip`：合订脚本、结构检查、视觉抽样图和发布 QA 收据。
- `OpenLogic_zh-Hans-CN_Evidence_Sanitized.zip` 与 `OpenLogic_zh-Hans-CN_Supplement80_Evidence.zip`：两部分的生产证据；前者是从不可改写的历史资产派生的隐私清理副本，旧版本字节仍保留在旧记录中。
- `README_Standalone722.md`：本说明。
- `Standalone722_SHA256SUMS.txt`：本次发布资产的字节数与 SHA-256。

既有主读本、补充读本、完整可编辑来源包及其证据包继续保存在同一 Zenodo 版本谱系和较早的 GitHub 发行版中，不因本次合订而删除或覆盖。重建本合订 PDF 需要 Python 3 与 `pypdf 6.10.0`；在包含两份哈希锁定输入 PDF 的原目录结构中运行 `build_combined_reader.py`。构建脚本会拒绝输入身份或页数变化，并在写出后重新打开结果。

## 已知限制

两份输入 PDF 均未标记结构标签，数学字体中仍有 8 行缺少 ToUnicode；因此本版不声称符合 PDF/UA，也不保证全部公式的复制、检索、抽取或屏幕阅读器语义。中文正文所用字体均嵌入且带 ToUnicode。该限制来自既有排版工具链，不影响本次证明的页面覆盖、视觉呈现或内部链接完整性。
