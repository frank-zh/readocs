.. _topics-标题:

================
Sphinx and RST
================

Sphinx简介
================

Sphinx 是一种文档工具，它可以令人轻松的撰写出清晰且优美的文档, 由 Georg Brandl 在BSD 许可证下开发. 新版的Python文档 就是由Sphinx生成的，
并且它已成为Python项目首选的文档工具,同时它对 C/C++ 项目也有很好的支持; 并计划对其它开发语言添加特殊支持. 本站当然也是使用 Sphinx 生成的，
它采用reStructuredText! Sphinx还在继续开发. 下面列出了其良好特性,这些特性在Python官方文档中均有体现:

- 丰富的输出格式: 支持 HTML (包括 Windows 帮助文档)、LaTeX (可以打印PDF版本)、manual pages（man 文档）和纯文本。
- 明晰的分层结构: 可以轻松的定义文档树,并自动化链接同级/父级/下级文章。
- 美观的自动索引: 可自动生成美观的模块索引。
- 精确的语法高亮: 基于 Pygments 自动生成语法高亮。
- 开放的扩展: 支持代码块的自动测试,并包含Python模块的自述文档(API docs)等。

rst简介
================

reStructuredText 是扩展名为.rst的纯文本文件，含义为"重新构建的文本"，也被简称为：RST或reST；是Python编程语言的Docutils项目的一部分，
Python Doc-SIG (Documentation Special Interest Group)。该项目类似于Java的JavaDoc或Perl的POD项目。
Docutils 能够从Python程序中提取注释和信息，格式化成程序文档。

.rst 文件是轻量级标记语言的一种，被设计为容易阅读和编写的纯文本，并且可以借助Docutils这样的程序进行文档处理，

也可以转换为HTML或PDF等多种格式，或由Sphinx-Doc这样的程序转换为LaTex、man等更多格式。
