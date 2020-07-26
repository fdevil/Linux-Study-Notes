.. :Author: ZQ
   :Contact: fdevilpublic@163.com
   :Revision: 1.0.0
   :Created Date: 2020-07-26
   :Modified Date:
   :Status: First draft
   :Copyright: This document has been placed in the public domain.
   
========
学习笔记
========

前言:

   这是第一次写博文，起源于一次linux系统的学习。学习过程中想把笔记记下来，防止忘记，意外在网上发现
   ``sphinx+restructuredText+github+readthedocs`` 写技术文档的各类资料博客，立刻被其强大的功能吸引，
   在后来的一段时间里，翻阅了无数的中文、英文（英文不行，全靠谷歌）资料，从头到尾实现了从 
   :guilabel:`Python`、:guilabel:`Sphinx`、:guilabel:`ReStructuredText`、:guilabel:`github`、:guilabel:`ReadTheDocs` 的全过程。
   在这里把它记录下来。

.. code::
   .. toctree::
      :maxdepth: 2    // 目录深度
      :hidden:        // 是否隐藏目录树，只显示左边索引
      :caption: Java  // 为目录树创建一个标题
      :numbered: 2    // 显示章节编号,会给所有的文件标题添加序号，只有第一个toctree能实现这个功能，最好不用
      :titlesonly:    // 只希望显示树中文档的标题，而不希望显示同一级别的其他标题


