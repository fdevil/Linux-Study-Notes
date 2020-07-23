.. restructuredtext-syntax documentation master file, created by
   zq on 2020.7.23.

reStructuredText语法
====================




This is a code
~~~~~~~~~~~~~~

This is a code
--------------

.. sourcecode:: rst

    .. toctree::
        :maxdepth: 1

        restructuredtext-syntax-copy
        哈哈 <restructuredtext-syntax-copy>
		
		
		
.. toctree::
    :maxdepth: 1

    restructuredtext-syntax-copy
	哈哈 <restructuredtext-syntax-copy>

----

.. note::

    this is a note.
	
.. tip::

    this is a tip.

.. warning::

    this is a warning.	
	
.. important::

    this is a important.	
	
.. code:: 

	$ system.output.printf("Hello Java!");

::

    this is a code 
	
.. sourcecode:: rst

    .. image:: your-image.png
        :alt: A description of this image

    .. figure:: your-image.png

        A caption for this figure
		
----

第一步
    连接一个 ``restructuredtext语法`` 文件，我的所有关于restructuredtext语法的内容都将在这个文件中
    展现出来，
	
	`单引号百度` \`单引号百度\` 
	
    *斜体百度* \*斜体百度*\
	
    **粗体百度** \*\*粗体百度\*\* 
	
    :guilabel:`百度1`
	
    ``百度2``  	
	
    `百度超链接 <https://www.baidu.com/>`_
	
    `百度4`_

    这是一套定义链接地址的自定义变量，上面只写变量  下面再给变量赋值，当多次调用时可用

    `百度4`_
	
	
.. _百度4: https://www.taobao.com/

----

This screencast will help you get started or you can
:ref:`Quick start超链接 <./restructuredtext-syntax:Quick start>`.





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
~~~~~~~~~~~
	
Quick start1
------------

Assuming you have Python already, `百度4`_ `hahah`_ fgfgffg `hahah`_ dfdfdf `install Sphinx`_

.. prompt:: bash $

    pip install sphinx
	
	
	
	
.. _hahah: https://www.taobao.com/
.. _install Sphinx: https://www.taobao.com/
	
.. raw:: html

    <div style="text-align: center; margin-bottom: 2em;">
    <iframe width="100%" height="350" src="https://www.bilibili.com/bangumi/play/ss33800?spm_id_from=333.851.b_62696c695f7265706f72745f616e696d65.54" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
	