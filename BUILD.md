# 可重复构建

单卷阅读器由两份分别构建的 PDF 无损合订：

- 主读本：744 页，642 个单元，SHA-256 `7110ACF6CD9FB3508D37F12842711546D286C18962CD2B20DACDF046AC2B595B`。
- 补充读本：124 页，80 个单元，SHA-256 `36625773FD455D33B03D2B922060CD71CE51C47082DFF1435B49D1F9DCD7A2C8`。

所用工具：MiKTeX 26.5（XeTeX 4.18、BibTeX 0.99e），Python 3.13 与 `pypdf 6.12.2`。

## 主读本

解压 `OpenLogic_zh-Hans-CN_Source.zip`，在 `locale/zh` 目录中依次运行：

```
xelatex -interaction=nonstopmode -halt-on-error -file-line-error -recorder -output-directory=BUILD open-logic-complete.tex
bibtex BUILD/open-logic-complete
xelatex ...（同上，共三遍）
```

`BUILD` 为输出目录，须预先建好其子目录 `content`。BibTeX 报告 `bib/open-logic.bib` 的六条警告，并因找不到 `content/open-logic-about.aux`（该单元没有文献引用）报告一条错误，以退出码 1 结束；最终日志无错误、未定义引用或未定义文献。

## 补充读本

解压 `OpenLogic_zh-Hans-CN_Supplement80_Source.zip`，在 `supplement/` 中运行 `build.ps1 -Stage full`（XeLaTeX、BibTeX（无引用时跳过）、再两遍 XeLaTeX），然后运行 `python check.py`。`check.py` 核对 80 个单元标记、31 个习题、216 个链接、来源哈希、缺字和日志警告。

## 合订

合订脚本 `assemble_combined.py` 在 `OpenLogic_zh-Hans-CN_Standalone722_Evidence.zip` 的 `combined/` 中：

```
python assemble_combined.py MAIN.pdf SUPPLEMENT.pdf OUTPUT.pdf RECEIPT.json
```

脚本逐页保留两份输入的内容流，把补充读本的 207 个内部命名链接改为明确页目标（两册有 201 个相同的目标名称），并导入两份书签树。写出后重新打开结果并检查：868 页均为 612 × 792 pt；868 个页面内容流与输入逐字节一致；3,145 个链接（80 个外部链接、2,858 个命名目标链接、207 个页目标链接）中，内部链接的目标均存在，所有链接矩形都在页面以内；书签父入口在第 1 页和第 745 页。输出 PDF 为 6,062,950 字节，SHA-256 `C464A9F8BBEA55D10D913DBBB4FF7FDD3D5A600B00236D9923EC7B50899496E0`。

## 英文术语括注检查

`combined/verify_pdf_glosses.py` 读取 `pdftotext -raw` 抽取的合订本文本，对每处括注检查“中文术语（英文”在全书中出现的次数。结果见 `combined/gloss-check.json`：923 处均恰好出现一次。
