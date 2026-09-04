# 《开放逻辑文本》大陆简体中文版：80 单元补充读本

本补充读本将原先只随可编辑源包提供的 80 个中文内容单元排成可检索的 123 页 PDF，与原有 736 页主读本配套使用。主读本选择 642 个来源单元；两册合计覆盖冻结清单中的全部 722 个来源单元。单元是源文件，不是页数，其中包括章节组织文件。

补充内容包括一阶逻辑的可推导性与极大一致集、可表示性、直觉主义与多值逻辑、λ 演算、非标准算术、正规模态逻辑，以及大篇幅的相继式演算、切割消去、自然演绎、正规化和命题即类型材料。也收录二阶逻辑、归纳定义及集合论的替代材料。原作者标明的草稿、实验性和未完成状态均保留；本册不是对原作者未写成内容的虚构补写。

## 阅读与覆盖

- [主读本 PDF（736 页，642 单元）](https://zenodo.org/records/22001949/files/OpenLogic_zh-Hans-CN_Complete.pdf)
- [补充读本 PDF（123 页，80 单元）](https://github.com/KokunoYumeto/open-logic-zh-hans-cn/releases/download/ZH-OLP-PUB-0004/OpenLogic_zh-Hans-CN_Supplement80.pdf)
- [Zenodo 版本集合](https://doi.org/10.5281/zenodo.21987817)
- [GitHub 项目](https://github.com/KokunoYumeto/open-logic-zh-hans-cn)

这次增补不覆盖原主读本或旧版文件。补充册保留 80 个单元自身的文字、标题、说明和公式；已在主读本出现的重复导入不再重复排印。所有 31 道显式习题均在相关正文后排印。已有完整证明予以保留，不因习题选项而隐藏。指向主读本的三处引用链接到确切版本的页面。

## 来源、许可与改动

原作：Open Logic Project，来源提交 `9620cc73f9c8e0ad003c514a5d3748f29611c4c0`。许可为 Creative Commons Attribution 4.0（CC BY 4.0）；包内保留原许可。译文为大陆取向简体中文（zh-Hans-CN），并非繁体中文、本地化新加坡版本或并排英文版本。

中文翻译与排版为 AI 生成，未经人工中文审校，不声称官方认可、同行评审、语言认证、PDF/UA 或数学无误。继承的英文与中文源文件保持不变，构建所需的精确修改仅应用于独立的补充册文件；`repairs.json` 逐项记录，包括来源记号错误、引用绑定和六处会隐藏证明的中文选择标签偏移。

正文使用宋体 10.5 TeX pt，行距 15.5 pt，左右页边距均为 0.85 英寸。自动检查确认 80 个单元各载入一次、31 道显式习题均出现、无未定义引用、缺字、重复标签、版面溢出或越界链接。生产者已检查全册缩略图及数学密集页的放大图。遗留数学字体仍有字号替代警告；PDF 未取得无障碍认证，数学公式的复制与辅助阅读能力不作保证。

## 重建

解压 `OpenLogic_zh-Hans-CN_Supplement80_Source.zip`。包中只携带此补充册实际需要的项目文件、80 个英文来源、80 个继承中文来源、覆盖清单及补充册脚本，不含系统字体、缓存、Git 元数据或凭据。

需要 Python 3、PyMuPDF、XeLaTeX 及相应 TeX 包，并安装宋体、微软雅黑、Times New Roman、Arial、Courier New。进入解压后的 `supplement` 目录运行：

```powershell
python prepare.py
pwsh -NoProfile -File build.ps1 -Stage full -MutexTimeoutMs 30000
python check.py
```

`build.ps1` 在 Windows 上使用全机共享的 TeX 互斥锁，并限制每个编译进程为 60 秒。无法取得锁时不启动编译器；不要平行启动第二份编译。没有引用命令时跳过 BibTeX。结果为 `supplement/build/reader.pdf`。不同 TeX 或字体版本可能改变换行和 PDF 字节；具体生成物由发布的 SHA-256 确定。
