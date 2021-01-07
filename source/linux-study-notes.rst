.. linux-study-notes.rst documentation master file, created by
   zq on 2021.1.7.

=======================
Linux学习笔记
=======================

.. contents:: 目录
   :depth: 3




Linux下常见文件介绍
=======================

| d /dev/dri 独立显卡驱动相关(unraid)。

| - /etc/passwd 用户相关信息
| - /etc/shadow 密码相关信息
| - /etc/group 用户组相关信息

| - /var/log/wtmp 用户登录数据记录,该文件是一个data file，能通过last命令读取，但是使用cat会读出乱码，属于一种特殊格式的文件(CentOS 5.x)。


Linux下常用命令
=======================

Linux ln 命令
-----------------------

.. code::

   ln [参数][源文件或目录][目标文件或目录]
   ln [源文件][目标文件或目录] // 硬链接，源文件只能是文件，目标可以是目录，即不更改文件名，不可以跨文件系统和硬盘。
   ln -s [源文件或目录][目标文件或目录] // 软链接，相当于windows下快捷方式，可以跨文件系统，跨硬盘。
