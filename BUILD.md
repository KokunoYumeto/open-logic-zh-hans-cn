# 可重复构建

本版本由两份已经冻结并分别验证的阅读器无损合订：

- `OpenLogic_zh-Hans-CN_Complete.pdf`：736 页，642 个常规驱动单元，SHA-256 `D1A7B35482973E6AEAF7FACFEB54E27870B407F069685B5309CD8BA04BF97F35`。
- `OpenLogic_zh-Hans-CN_Supplement80.pdf`：123 页，其余 80 个单元，SHA-256 `DECED432302472F951E0016230310DEB3513CC8FBF4D269559554672B025610C`。

从发行版下载并解压两个可编辑来源包，可分别重建两份输入 PDF。主读本使用 XeLaTeX 与 BibTeX；补充读本来源包中的 `build.ps1` 使用全机 TeX 互斥锁，并给出完整的依赖、命令和检查说明。

合订步骤只需 Python 3 与 `pypdf 6.10.0`：保持证据包中的目录关系，把两份哈希锁定 PDF 放在脚本声明的位置，然后运行：

```powershell
python build_combined_reader.py
python verify_combined_reader.py
```

合订脚本拒绝输入哈希或页数变化。它逐页保留渲染内容，把补充册 207 个内部命名链接改为明确页目标，以免两册共有的 200 个目标名称引起错跳，并导入两份书签树。确定性重放两次得到完全相同的 5,975,161 字节 PDF，SHA-256 为 `1EAFF4694F18893E49AFD020F6F4FF1ED5B90B29755A24B011E53B759B27AF19`。

验证结果：859 页均为 612 × 792 pt；859 个页面内容流与输入逐页一致；3,136 个链接全部保留，无未解析目标或越界矩形；书签父入口分别指向第 1 页和第 737 页。144 dpi 视觉抽样检查了第 1、101、736、737、738、799 和 859 页。详细结果及抽样图在 `OpenLogic_zh-Hans-CN_Standalone722_Evidence.zip`。

PDF 未标记结构标签，且 68 行字体中有 8 行遗留数学字体缺少 ToUnicode，因此不声称 PDF/UA 或完整公式抽取能力。中文正文字体均嵌入并带 ToUnicode。
