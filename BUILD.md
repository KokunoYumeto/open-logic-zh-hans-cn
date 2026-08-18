# 可重复构建

构建根：源包中的 `locale/zh`。工具链：MiKTeX XeLaTeX 26.5 与 BibTeX 0.99e。

```powershell
xelatex -interaction=nonstopmode -halt-on-error -file-line-error -output-directory=<build> open-logic-complete.tex
bibtex <build>/open-logic-complete
xelatex -interaction=nonstopmode -halt-on-error -file-line-error -output-directory=<build> open-logic-complete.tex
xelatex -interaction=nonstopmode -halt-on-error -file-line-error -output-directory=<build> open-logic-complete.tex
xelatex -interaction=nonstopmode -halt-on-error -file-line-error -output-directory=<build> open-logic-complete.tex
```

中文正文在 `locale/zh/open-logic-complete.tex` 中明确设为 10.5 pt / 15.5 pt，主字体为 SimSun。最终 PDF 为 1,013 页。

最终日志无致命错误、未定义引用、未定义文献、缺字、重复标签、重跑请求或页眉高度警告。82 个 overfull hbox 来自长公式或不可断行标识；最宽的实物页经检查仍在 612 pt MediaBox 内。BibTeX 的六条上游书目数据警告及 PDF 无障碍限制见证据包 `qa.json`。
