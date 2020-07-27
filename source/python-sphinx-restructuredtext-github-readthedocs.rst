.. :Author: ZQ
   :Contact: fdevilpublic@163.com
   :Revision: 1.0.0
   :Created Date: 2020-07-26
   :Modified Date:
   :Status: First draft
   :Copyright: This document has been placed in the public domain.
   
============================================================
Python+sphinx+restructuredtext+github+readthedocs写技术文档
============================================================
:Date: 2020-07-26

.. contents:: 目录
   :depth: 3

前言
=====

这是第一次写博文，起源于一次Linux系统的学习。学习过程中想把笔记记下来，防止忘记，意外在网上发现
``sphinx+reStructuredText+github+readthedocs`` 写技术文档的各类资料博客，立刻被其强大的功能吸引，
在后来的一段时间里，翻阅了无数的中文、英文（英文不行，全靠谷歌）资料，从头到尾验证了从 
:guilabel:`Python`、:guilabel:`pip`、:guilabel:`Sphinx`、:guilabel:`reStructuredText(rst)`、
:guilabel:`github`、:guilabel:`ReadTheDocs` 的全过程。在这里把所学的知识、所遇到的困难、
所解决的问题记录下来。



sphinx+reStructuredText+github+readthedocs简介
==============================================

什么是sphinx、rst?
------------------

什么是.md、.rst?
----------------

**reStructuredText** 是扩展名为 ``.rst`` 的纯文本标记语法。**markdown** 是拓展名为 ``.md`` 的纯文
本文件。reStructuredText是一个易于阅读的，看到的是什么您可以得到的纯文本标记语法和解析器系统。它对于
内联程序文档（例如Python docstrings），快速创建简单的网页以及独立文档很有用。reStructuredText设计用
于特定应用程序域的可扩展性。reStructuredText解析器是Docutils的组件 。reStructuredText是对StructuredText
和Setext轻量级标记系统的修订和重新解释 。reStructuredText的主要目标是定义和实现供Python文档字符串和其
他文档领域使用的标记语法，该语法易读且简单，但足够强大，可以轻松使用。标记的预期目的是将reStructuredText
文档转换为有用的结构化数据格式。[#什么是rst]_

什么是github、git、readthedocs?
-------------------------------

安装python
===========

安装sphinx
===========

reStructuredText语法
====================

github托管文档
==============

git的使用
-----------

readthedocs部署文档
===================

readthedocs自动配置文档
-----------------------

readthedocs手动配置文档
-----------------------

引用文献
========

.. [#什么是rst] https://www.jianshu.com/p/0dc1eb6feea6