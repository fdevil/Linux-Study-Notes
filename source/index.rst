.. Linux-Study-Notes documentation master file, created by
   sphinx-quickstart on Wed Jul 15 14:52:01 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

========
学习笔记
========

.. code::
   .. toctree::
      :maxdepth: 2    // 目录深度
      :hidden:        // 是否隐藏目录树，只显示左边索引
      :caption: Java  // 为目录树创建一个标题
      :numbered: 2    // 显示章节编号,会给所有的文件标题添加序号，只有第一个toctree能实现这个功能，最好不用
      :titlesonly:    // 只希望显示树中文档的标题，而不希望显示同一级别的其他标题



.. toctree::
   :numbered: 2
   :maxdepth: 2
   :caption: Hello Sduty Notes

.. 
   /index
   
   
..    
.. toctree::
   :numbered: 2
   :caption: Test numbered
..
   /index
   
   
.. 
.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: First notes
..
   /restructuredtext-syntax
   /python-pip-sphinx-restructuredtext-vscode


.. 
.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Second notes
..
   /python-pip-sphinx-restructuredtext-vscode

- :doc:`python-pip-sphinx-restructuredtext-vscode`
- :doc:`restructuredtext详细语法 <restructuredtext-syntax>`
- :doc:`restructuredtext-syntax-copy`



二级标题
============

哈哈哈 :ref:`Git Setup <setup>` 大幅度
