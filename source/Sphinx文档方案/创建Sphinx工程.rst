.. _topics-标题:

================
创建Sphinx工程
================

本章节介绍如何使用sphinx和rst创建及发布一个文档工程。

创建文档工程
================

#.  在本地新建一个Sphinx项目文件夹。
#.  打开命令行终端(例如，Windows CMD), 进入项目文件夹。
#.  输入以下命令，进入项目创建流程。

.. code-block:: bash

		sphinx-quickstart

4.  参考以下内容，创建项目:

.. code-block:: bash

        You have two options for placing the build directory for Sphinx output.
        Either, you use a directory "_build" within the root path, or you separate
        "source" and "build" directories within the root path.
        > Separate source and build directories (y/n) [n]: y

        Inside the root directory, two more directories will be created; "_templates"
        or custom HTML templates and "_static" for custom stylesheets and other static
        files. You can enter another prefix (such as ".") to replace the underscore.
        > Name prefix for templates and static dir [_]:

        The project name will occur in several places in the built documentation.
        > Project name: Test
        > Author name(s): Zhaojiedi1992

        Sphinx has the notion of a "version" and a "release" for the
        software. Each version can have multiple releases. For example, for
        Python the version is something like 2.5 or 3.0, while the release is
        something like 2.5.1 or 3.0a1.  If you don't need this dual structure,
        just set both to the same value.
        > Project version []: v1.0
        > Project release [v1.0]:

        If the documents are to be written in a language other than English,
        you can select a language here by its language code. Sphinx will then
        translate text that it generates into that language.

        For a list of supported codes, see
        http://sphinx-doc.org/config.html#confval-language.
        > Project language [en]: en

        The file name suffix for source files. Commonly, this is either ".txt"
        or ".rst".  Only files with this suffix are considered documents.
        
        A Makefile and a Windows command file can be generated for you so that you
        only have to run e.g. `make html' instead of invoking sphinx-build
        directly.
        > Create Makefile? (y/n) [y]:
        > Create Windows command file? (y/n) [y]:

        Creating file .\source\conf.py.
        Creating file .\source\index.rst.
        Creating file .\Makefile.
        Creating file .\make.bat.

        Finished: An initial directory structure has been created.

        You should now populate your master file .\source\index.rst and create other documentation
        source files. Use the Makefile to build the docs, like so:
        make builder
        where "builder" is one of the supported builders, e.g. html, latex or linkcheck.

5.  进入工程文件目录,然后进入Source文件夹。该文件夹包含几个文件。其中Index.rst用于设置文档TOC， conf是Sphinx的配置文件，可以配置输出文档的主题。可以新建.rst文件，编辑文档内容。

具体文档编写语法，参考以下链接内容：

- `sphinx对rst文档的帮助文档 <http://www.sphinx-doc.org/en/stable/rest.html>`_    
- `rst的官文帮助文档 <http://docutils.sourceforge.net/rst.html>`_

设置主题
================

Sphinx提供默认主题。如果需要下载更多主题，参考: `官方内置主题 <http://www.sphinx-doc.org/en/stable/theming.html#builtin-themes>`_

此处以sphinx_rtd_theme主题为例进行安装。进入Source目录，执行下面命令：

.. code-block:: bash

		pip install sphinx_rtd_theme

安装完毕后，修改conf.py文件，保存。

.. code-block:: bash

		html_theme = 'sphinx_rtd_theme'

生成文档
================

在工程目录（非source目录），执行make命令：

.. code-block:: bash

		make html

预览文档
================

生成的htm目录在工程的build/html目录下。双击html目录下的index.html完成预览。