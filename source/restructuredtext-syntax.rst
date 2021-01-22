====================
reStructuredText语法
====================
:Author: ZQ
:Contact: fdevilpublic@163.com
:Revision: 1.0.0
:Date: 2020-07-24
:Copyright: This document has been placed in the public domain.
:Status: First draft
:haha: nihoa

常见语法
========

这是一个标题
------------

这是一个标题

.. code::

   .. toctree::
      :maxdepth: 2    // 目录深度
      :hidden:        // 是否隐藏目录树，只显示左边索引
      :caption: Java  // 为目录树创建一个标题
      :numbered: 2    // 显示章节编号,会给所有的文件标题添加序号，只有一个文档只能一个toctree能实现这个功能，最好不用
      :titlesonly:    // 只希望显示树中文档的标题，而不希望显示同一级别的其他标题
   

.. contents:: 目录
   :local: 
   :backlinks: none
   :depth: 1

.. contents::

.. code代码有 rst java jawl等

.. code:: rst           

    .. contents:: 目录3  //目录,冒号后空格接“目录”,会在主页上显示为“目录”,不接“目录”，将显示“contents”.
        :local:
        :backlinks: none // none 1 2 3
        :depth: 1 //展示目录级数

.. code-block:: rest
   
   .. code-block:: rest

      :linenos:                             // 生成行号
      :lineno-start: number (number)        、、


.. sourcecode:: rst

    .. toctree::
        :maxdepth: 1
        :hidden:
        :caption: Step-by-step Guides
        
        restructuredtext-syntax-copy
        哈哈 <restructuredtext-syntax-copy>


.. code:: rst

    .. adasda
    asdasd
    asd

        
        

----

.. _setup:

.. attention:: this is a attention,这是一个注意
.. caution:: this is a caution,这是一个警告
.. danger:: this is a danger,这是一个危险
.. error:: this is a error,这是一个错误
.. hint:: this is a hint,这是一个提示
.. important:: this is a important,这是一个重要
.. note:: this is a note,这是一个注解
.. tip:: this is a tip,这是一个小建议
.. warning:: this is a warning,这是一个警告
.. title:: this is a title,这是一个标题

.. admonition:: 大家要注意啊

   这是一个自定义的提示框

.. topic:: Topic Title

    Subsequent indented lines comprise
    the body of the topic, and are
    interpreted as body elements.

.. sidebar:: Sidebar Title
   :subtitle: Optional Sidebar Subtitle

   Subsequent indented lines comprise
   the body of the sidebar, and are
   interpreted as body elements.

.. csv-table:: Frozen Delights!
   :header: "Treat", "Quantity", "Description"
   :widths: 15, 10, 30

   "Albatross", 2.99, "On a stick!"
   "Crunchy Frog", 1.49, "If we took the bones out, it wouldn't be
   crunchy, now would it?"
   "Gannet Ripple", 1.99, "On a stick!"

.. list-table:: Frozen Delights!
   :widths: 15 10 30
   :header-rows: 1

   * - Treat
     - Quantity
     - Description
   * - Albatross
     - 2.99
     - On a stick!
   * - Crunchy Frog
     - 1.49
     - If we took the bones out, it wouldn't be
       crunchy, now would it?
   * - Gannet Ripple
     - 1.99
     - On a stick!

.. |date| date::
.. |time| date:: %H:%M

Today's date is |date|.

This document was generated on |date| at |time|.

.. code:: java

    $ system.out.printf("Hello Java!");

::

    this is a code 
    this is a code
    这是一个文字块
    
.. sourcecode:: rst

    .. image:: your-image.png
        :alt: A description of this image

    .. figure:: your-image.png

        A caption for this figure
        
----

文字样式:
    连接一个 ``restructuredtext语法`` 文件，我的所有关于restructuredtext语法的内容都将在这个文件中，

    展现出来，
    
    `单引号百度` \`单引号百度\` 
    
    *斜体百度* \*斜体百度*\
    
    **粗体百度** \*\*粗体百度\*\* 
    
    :guilabel:`百度1`
    
    ``百度2``    

.. "|"行块，相当于强制换行符。

| 不使用换行符“|”

窗前明月光
疑是地上霜
举头望明月
低头思故乡

| 使用换行符“|”
| 窗前明月光
| 疑是地上霜
| 举头望明月
| 低头思故乡  
    
外部超链接：    
    `百度超链接 <https://www.baidu.com/>`_
    
    `百度4`_

    这是一套定义链接地址的自定义变量，上面只写变量  下面再给变量赋值，当多次调用时可用



    `百度4`_
    
    不空`百度超链接 <https://www.baidu.com/>`_哈哈`百度4`_哈哈 百度4_ 哈哈百度4_哈哈
    
    空格 `百度超链接 <https://www.baidu.com/>`_ 哈哈 `百度4`_ 哈哈 百度4_ 哈哈百度4_哈哈


.. _百度4: https://www.taobao.com/

内部超链接,内部超链接也可以接https://www.baidu.com，作为外部超链接使用：

    `百度5`_

.. _百度5: ./index.html

.. 批量链接，上下数量要一致，如果没有段落，则顶格，嵌套则缩进

- `百度`__
- `搜狐`__
- `淘宝`__
- `新浪`__
   

__ https://www.baidu.com
__ https://www.sohu.com
__ https://www.taobao.com
__ https://www.sina.com

这是我的 `引用文献`_ 锚链接空格，我的引用 [#我的标准]_
这是我的`引用文献`_锚链接不空格

----

.. This screencast will help you get started or you can
.. :ref:`Quick start超链接 <restructuredtext-syntax:Quick start>`.




----

.. image:: /_static/images/profile-photo.jpg
    :alt: A description of this image

.. figure:: ./_static/images/dog.png
    :align: center
    :figwidth: 80%
    :target: ./_static/images/dog.png

    漂亮的狗狗,这个是图片的描述，描述和图片地址代码空一行哦，不然会出错

    
.. note::

    文档中source下建立的图片文件夹images在构建过程中在主目录下新建_images，并将所有的图片都拷贝在该文件夹下，
    而在source/_static下建立images文件夹，依然会被拷贝在_images下，也会在./_static/images下
    

Quick start
-----------
    
Quick start1
~~~~~~~~~~~~

    
.. raw:: html

    <div style="text-align: center; margin-bottom: 2em;">
    <iframe width="100%" height="350" src="https://www.bilibili.com/bangumi/play/ss33800?spm_id_from=333.851.b_62696c695f7265706f72745f616e696d65.54" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
    

sdsd

----

:guilabel:`百度1`

----

:download:`can download conf <./conf.py>`

----

:kbd:`C-x C-f`

----

:kbd:`Control-x Control-f`

----

:abbr:`LIFO (last-in, first-out)`

----

:mailheader:`Content-Type`

----

:manpage:`ls(1)`

----

|today|

----

|version|

----

|release|





引用文献
========

.. [#] Python's creator and "Benevolent Dictator For Life"，Guido van Rossum.
.. [#] 哈哈哈的书籍.
.. 这种写法[#引用网页] 依然不会显示"引用网页"几个字

.. [#引用网页] The second draft of the spec:
.. [#我的标准] 我的标准。


引用参考的内容通常放在页面结尾处，比如 [One]_，Two_, Three_, fore_

脚注引用一 [1]_
脚注引用一 [2]_
脚注引用二 [#]_
脚注引用三 [#链接]_
脚注引用四 [*]_
脚注引用五 [*]_
脚注引用六 [*]_



.. [1] 脚注内容一
.. [2] 脚注内容二
.. [#] 脚注内容三
.. [#链接] 脚注内容四 链接_
.. [*] 脚注内容五
.. [*] 脚注内容六
.. [*] 脚注内容七




.. [One] 参考引用一
.. [Two] 参考引用二
.. [Three] `简书超链接 <https://www.jianshu.com/>`_
.. [fore] `https://www.jianshu.com/`_