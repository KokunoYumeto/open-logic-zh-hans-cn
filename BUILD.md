# 可重放构建

来源身份：Open Logic Project 提交 `9620cc73f9c8e0ad003c514a5d3748f29611c4c0`。

解压 `OpenLogic_zh-Hans-CN_Source.zip`，进入 `locale/zh`，依次运行：

```text
xelatex -interaction=nonstopmode -halt-on-error -file-line-error open-logic-complete.tex
bibtex open-logic-complete
xelatex -interaction=nonstopmode -halt-on-error -file-line-error open-logic-complete.tex
xelatex -interaction=nonstopmode -halt-on-error -file-line-error open-logic-complete.tex
```

生产环境为 MiKTeX XeLaTeX 26.5。中文正文使用宋体，中文黑体使用微软雅黑；若系统没有这些字体，必须明确替换字体并把替换记录为新的构建变体，不能沿用本发布 PDF 的哈希。

最终 PDF：3,919,880 字节，SHA-256 `CEDE048997A9061E8F64EBBE82D49C8BAF8B631B9A13E1CA98B5F85C4ABF9878`，873 页。完整检查结果见证据包内 `qa.json`。
