.. python-pip-sphinx-restructuredtext-vscode documentation master file, created by
   zq on 2020-07-24.You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


=================================================
python+pip+sphinx+restructuredtext+vscode学习笔记
=================================================

这是一个关于学习的笔记

一、restructuredtext语法
----------------------------

:doc:`restructuredtext语法1 <restructuredtext-syntax>`

:doc:`/restructuredtext-syntax-copy`

这两种语法的区别 **:doc:\`restructuredtext语法1 <restructuredtext-syntax>\`**   可以指定显示链接文字restructuredtext语法1

**:doc:\`/restructuredtext-syntax-copy\`** 取文件restructuredtext-syntax-copy的标题为链接文字

dfsd :ref:`restructuredtext-syntax <测试readthedocs自动构建>` .

This screencast will help you get started or you can
:ref:`read our guide below <restructuredtext-syntax:Quick start1>`.

----


第一步
    连接一个 ``restructuredtext语法`` 文件，我的所有关于restructuredtext语法的内容都将在这个文件中
	展现出来，
	:guilabel:`百度`
	
二哈哈
    djfksjdfkjsdkfjskdfjskdfjskdfjksdjfksjfdksjfksjdfksjdfksjdfksjdkfjsdf
	sdf
	sdf

二、指数和表格
------------------

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

三、restructuredTest语法
---------------------------

.. 分割线（四条及以上短线）

---- 

一、代码块
~~~~~~~~~~~~~~

----

四、Using the generic API integration2
------------------------------------------

这个是测试

一、Using the generic API integration3
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This endpoint accepts the following arguments during an HTTP POST:

**1、**

格式："::"(双冒号，空一行，缩进代码,或者空格，不能顶格写)

示例::

    示例::
        
        // 临时更换pip数据源
        pip install sphinx_rtd_theme -i https://pypi.tuna.tsinghua.edu.cn/simple
	

**2、**
	
.. note::
    哈哈哈
	
.. note:
    哈哈哈

.. note
    哈哈哈	


**3、**

Run ``sphinx-quickstart`` in there:

**4、**

.. meta::
   :description lang=en: Automate building, versioning, and hosting of your technical documentation continuously on Read the Docs.





	
---- 

二、标题

----


坚持以 ``习近平`` 总书记在 `中央城市` 管理工作会议上讲话精神为指导，

* 以服务民生为宗旨，
* 以提升城市品质和形象为目标，
* 以城市精细化管理为抓手，
* 以百度为查询 ``https://www.baidu.com``

1. 以服务民生为宗旨，
#. 以提升城市品质和形象为目标，
#. 以城市精细化管理为抓手，
#. 有序列表以1. 2. 3. 4. ......    或者1. #. #. #. ......
#. 有序列表5

在梁平区主要车站周边实施市容环境秩序综合整治，
着力营造“:guilabel:`干净整洁有序`、:guilabel:`山清水秀城美`、:guilabel:`宜居宜业`”的城市环境，
不断增强人民群众的幸福感、获得感。














测试readthedocs自动构建
---------------------------


python -m pip install --upgrade pip //更新pip

pip install sphinx //安装sphinx

pip install sphinx -i https://pypi.tuna.tsinghua.edu.cn/simple

pip install sphinx-autobuild //可以构建一个本地的服务  127.0.0.1/8000在浏览器中访问，端口不记得了

pip install sphinx_rtd_theme //安装主题

pip install sphinx_rtd_theme -i https://pypi.tuna.tsinghua.edu.cn/simple

pip install sphinx -i https://pypi.tuna.tsinghua.edu.cn/simple

pip临时换源提升下载速度其实你只要加个参数 -i，可能就会让下载速度上升 10 倍，比如：

pip install django -i https://pypi.tuna.tsinghua.edu.cn/simple

后面的地址可以换成国内的 pip 镜像：

清华 https://pypi.tuna.tsinghua.edu.cn/simple \br
中科大 https://pypi.mirrors.ustc.edu.cn/simple

阿里云 https://mirrors.aliyun.com/pypi/simple

豆瓣 http://pypi.douban.com/simple

::
	pip install sphinx_rtd_theme -i https://pypi.tuna.tsinghua.edu.cn/simple
	1
	
::

	pip install sphinx_rtd_theme -i https://pypi.tuna.tsinghua.edu.cn/simple
	2


.. “人生的意志和劳动将创造奇迹般的奇迹。”

	— 涅克拉索
	

下面是一个代码块::
	pip install sphinx_rtd_theme -i https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html


	
测试网络钩子是否运行1 2 3 4
--------------------------------

Webhooks / Manage webhook     /Secret
------------------------------------------

057dd908c422af3f1bd70178de73e6d0f93c92c26a4ab690c95ab5865d034a49cb2cbf73c29cc9879c18f7370a166151769517e1c0186a5c5515a329719a3f46






vscode 安装错误选择
selcet how to generate html from rst files


Windows 系统如何完全卸载 VSCode
文章目录
Windows 系统如何完全卸载 VSCode
0. 参考资料
1. 删不干净的用户数据
2. 解决方案
0. 参考资料
Uninstall visual studio code in windows
1. 删不干净的用户数据
最近正在从 Sublime Text 3 环境切换到 VS Code，看重的是后者的开源、免费、跨平台等特性，以及强大的后台与广泛的用户群。
但是对 VS Code 的一次卸载重装之后，我发现之前的插件和配置还在，不禁感叹这么多年了，微软还是没有学会软件的正确卸载姿势，只能自己动手将其卸载干净了。

2. 解决方案
注意：以下步骤需要在执行 VSCode 自带卸载程序之后执行。

win + r 打开运行
%appdata% 回车
删除 Code 和 Visual Studio Code 文件夹
地址栏输入 %userprofile% 回车
删除 .vscode 文件夹

https://blog.csdn.net/jpch89/article/details/89789247
版权声明：本文为CSDN博主「团子大圆帅」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/jpch89/java/article/details/89789247

