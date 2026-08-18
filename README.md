# 开放逻辑项目：《开放逻辑文本》完整大陆简体中文版

Open Logic Project — Complete Mainland Simplified-Chinese Edition (`zh-Hans-CN`)

## 直接阅读

- 完整度：722/722 个锁定的来源对应内容 TeX 单元（100%）
- 语言：大陆取向简体中文（`zh-Hans-CN`）
- 阅读器：873 页、可检索的 US Letter PDF
- 来源：Open Logic Project 提交 `9620cc73f9c8e0ad003c514a5d3748f29611c4c0`
- 许可：CC BY 4.0

这是 Open Logic Project 锁定来源树的完整大陆简体中文翻译。上游完整构建选择 642 个内容单元；另外 80 个已翻译的草稿、替代或未由完整构建选择的单元仍保存在可编辑源包中，未被遗漏或冒充为已渲染页面。

原作与作者：Open Logic Project。中文翻译与排版：AI typesetting & translation，由 OpenAI 5.6 Sol（Ultra mode）在 Floris 指导下完成。本版尚未经人工中文审校，不声称是同行评审版、批判版、Open Logic Project 官方中文版、无障碍认证版或 PDF/UA 版，也不表示原作者或相关机构认可。

## 文件

- `OpenLogic_zh-Hans-CN_Complete.pdf`：当前完整中文阅读器。
- `OpenLogic_zh-Hans-CN_Source.zip`：完整可编辑来源树，不含任何 Git 元数据。
- `OpenLogic_zh-Hans-CN_Evidence.zip`：清单、变更、术语、跨中日韩韩语体候选、QA 与来源身份收据。
- `SHA256SUMS.txt`：发布资产的精确字节数与 SHA-256。

## 构建与已知限制

使用 XeLaTeX 与 BibTeX 构建；详细命令见 `BUILD.md`。最终构建无致命错误、未定义引用、未定义文献、缺字、重复标签或重跑请求。PDF 未标记，且 7 个数学或 Type 3 字体行没有 ToUnicode，因此不对公式复制、检索、抽取或屏幕阅读器结构作无障碍合格声明。完整机器收据在证据包的 `qa.json` 中。

英文只保留于来源书名、专名、文献条目、代码、公式和稳定标识；它不是并列的英文版本。
