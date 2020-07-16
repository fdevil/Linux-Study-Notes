.. Linux-Study-Notes documentation master file, created by
   sphinx-quickstart on Wed Jul 15 14:52:01 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.打发打发

Welcome 龙妹妹 终于把这个弄好了，嘿嘿嘿
=============================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:



指数和表格
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

测试readthedocs自动构建
========================


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
	
	
..

	“人生的意志和劳动将创造奇迹般的奇迹。”

    — 涅克拉索
	
	
测试网络钩子是否运行1 2 3 4
==========================================

Webhooks / Manage webhook     /Secret
=====================================
057dd908c422af3f1bd70178de73e6d0f93c92c26a4ab690c95ab5865d034a49cb2cbf73c29cc9879c18f7370a166151769517e1c0186a5c5515a329719a3f46