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

| d /etc/init.d             服务service所在目录
| - /etc/passwd             用户相关信息
| - /etc/shadow             密码相关信息
| - /etc/group              用户组相关信息
| - /etc/crontab            任务调度与例行性工作相关
| - /etc/cron.deny          不允许使用cron调度指令的用户，一个用户一行
| - /etc/fstab              永久挂载磁盘、U盘等，添加完成后执行mound -a 即可生效
| - /etc/sysconfig/network-scripts/ifcfg-eth0   网卡ip等配置文件，不同网卡最后的命名不一样
| - /etc/hostname           主机名
| - /etc/inittab            运行级别相关信息
| - /etc/profile            设置环境变量
| - /etc/rsyslog.conf       日志相关 CentOS7
| - /etc/logrotate.conf     全局的日志轮替策略、规则，也可以单独给某个日志文件指定策略

| - /var/log/wtmp 用户登录数据记录,该文件是一个data file，能通过last命令读取，但是使用cat会读出乱码，属于一种特殊格式的文件(CentOS 5.x)。

| d /usr/lib/systemd/system systemctl指令管理的服务在/usr/lib/systemd/system目录下查看


Linux下常见服务介绍
=======================

* atb                       at任务调度与例行性工作服务
* crond                     crontab任务调度与例行性工作服务









Linux下常用命令
=======================

Linux ln 命令
-----------------------

.. code::

   ln [参数][源文件或目录][目标文件或目录]
   ln [源文件][目标文件或目录] // 硬链接，源文件只能是文件，目标可以是目录，即不更改文件名，不可以跨文件系统和硬盘。
   ln -s [源文件或目录][目标文件或目录] // 软链接，相当于windows下快捷方式，可以跨文件系统，跨硬盘。


vi和vim快捷键
================

* 复制当前行 yy,复制当前行向下5行 5yy,并粘贴（输入p）.
* 删除当前行 dd,删除当前行向下5行 5dd.
* 在文件中查找某个单词 /查找的单词,回车查找,输入n查找下一个.
* 设置和取消文件的行号, :set nu 和 :set nonu.
* 编辑/etc/profile文件,使用快捷键到该文档的最末行[G]和最首行[gg].
* 在一个文件中输入“Hello”,然后又撤销这个动作[u].
* 编辑/etc/profile文件,并将光标移动到20行,一般模式下输入20再按[shift+g].

关机&重启命令
===============

基本介绍

* shutdown -h now   立刻关机
* shutdown -h 1     通知登录用户，1分钟后关机
* shutdown -r now   立刻重启
* halt              关机，作用和上面一样
* reboot            立刻重启
* sync              把内存的数据同步到磁盘

注意细节

* 不管是重启系统还是关闭系统，首先要运行sync命令，把内存中的数据写到磁盘中。
* 目前shutdown/halt/reboot等命令均已经在关机前进行了sync。不过小心使得万年船。

用户登录和注销
================

基本介绍

* su - 用户名,命令来切换账户
* logout命名注销账户，在图形界面运行无效，在运行级别3血有效。

用户管理
==========

添加用户
---------

* useradd 用户名    创建用户
* useradd -d /root/haha 用户名   指定家目录

* userdel 用户名     删除用户，保留家目录
* userdel -r 用户名  删除用户，-r删除家目录

* passwd 用户名          修改某用户密码

* pwd  查看当前所在目录

* id 用户名          查询用户的信息
* su - 用户名        切换用户，高权限到低权限用户不用输入密码
* whoami              查看当前登录用户
* who am i             查看第一次登录用户详细信息，切换用户后依然显示第一次登录的用户


用户组
========

* groupadd 组名         新增组
* groupdel 组名         删除组
* useradd -g 用户组 用户名   增加一个用户，直接将它指定到用户组


例行行工作与任务调度
=====================

Linux工作调度的种类：at,crontab

at:at是个可以处理仅执行一次就结束调度的命令，不过要执行at时，必须要求atd这个服务的支持，在某些新版的distributions中，atd可能默认没有启动，那么at命令就会失效，不过CentOS默认是启动的。

crontab:crontab所设置的任务将循环一直进行下去，除了使用crontab命令执行外，也可以编辑/etc/crontab文件来支持，让crontab生效则需要crond这个服务支持。

-e 编辑任务
-l 查询任务
-r 删除任务



磁盘与目录
=============


* lsblk 查看所有分区挂载情况
* lsblk -f 查看所有分区挂载情况 -f显示具体参数
* df -h 查看系统整体磁盘使用情况
* du -h /目录     // 查询指定目录的磁盘占用情况
    - -s 指定目录占用大小汇总
    - -h 带计量单位
    - -a 含文件
    - -c 列出明细的同时，增加汇总值
    - --max-depth=1 子目录深度
* ls -l /opt | grep "^-" | wc -l        // 统计/opt文件夹下文件的个数
* tree  //以目录显示   如果没有yum install tree安装，

网络配置
===========

* /etc/sysconfig/network-scripts/ifcfg-eth0 网卡ip等配置文件，不同网卡最后的命名不一样
* service network restart              // 修改网络配置后，重启网络服务
* hostname      查看主机名

进程
========
ps

* -e 显示所有进程
* -f 全格式
* -a
* -u 
* -x

ps -ef 查看进程
ps -aux 常用经常查看命令


终止进程kill和killall

kill [选项] 进程号 // 通过进程号终止进程
killall 进程名称 // 通过进程名终止进程，也支持通配符，这在系统因负载过大而变得很慢时很有用。

[选项]
* -9 强制终止进程

案例

* 

pstree 查看进程数
-p 显示进程号
-u 显示进程用户

服务(service)管理
=====================

基本介绍
---------

服务(service)本质就是进程，但是是运行在后台的，通常都会监听某个端口，等待其他程序
的请求，比如(mysqld,sshd,防火墙等)，因此又称为守护进程，是Linux中非常重要的知识点。

service管理指令
------------------

* service 服务名 [start|stop|restart|reload|status]
* 在CentOS7.0后很多服务不再使用service，而是systemctl。
* service指令管理的服务在/etc/init.d目录下查看
* ls -l /etc/init.d // 查看service管理的服务
* setup // 命令查看所有服务，带*号的为随系统启动

systemctl 命令
---------------

* 基本语法:systemctl [start|stop|restart|status] 服务名
* systemctl指令管理的服务在/usr/lib/systemd/system目录下查看
* systemctl list-nuit-files [| grep 服务名] // 查看服务开机启动状态，grep进行过滤
* systemctl enable 服务名 // 设置服务开机启动，永久生效，在3/5级别生效
* systemctl disable 服务名 // 关闭服务开机启动，永久生效，在3/5级别生效
* systemctl is-enabled 服务名 // 查询某个服务是否是自启动





systemctl get-default // 查看当前运行级别

systemctl set-default graphical.target // 设置当前级别为图形化级别，也就是级别5


chkconfig 命令

* 通过命令可以给服务的各个运行级别设置自 启动|关闭
* chkconfig指令管理的服务在/etc/init.d查看
* 注意：在CentOS7.0后，很多服务使用systemctl管理
* chkconfig重新设置服务自启动和关闭，需要重新启动reboot生效。

chkconfig --list 查看服务
chkconfig 服务名 --list 查看某服务
chkconfig --level 5 服务名 on|off 设置某服务在5级别下自启动|自关闭

rpm包的管理
==============

* rpm -qa  // 查询所有安装的rpm软件包
* rpm -q 软件包  // 查询是否安装某软件包
* rpm -qi 软件包名  // 查询某软件包详细信息
* rpm -qf 文件全路径 // 查询文件所属的软件包，也就是文件由那个软件所生成的
* rpm -qf /etc/passwd // 查/etc/passwd 由那个软件包生成
* rpm -e 软件包 // 删除软件包，如果该软件包被依赖，将提示
* rpm -e --nodeps 软件包 // 强制删除软件包

* rpm -ivh 软件包全路径名称   // 安装软件包 i=install安装 v=verbose提示 h=hash进度条

yum
=====

yum是一个Shell前段软件包管理器，给予RPM包管理，能够从指定的服务器自动下载RPM包并且安装，
可以自动处理依赖性关系，并且一次安装所有依赖的软件包。

yum list | grep xx xx软件列表
yum install xxx 下载xxx安装，并安装所有的依赖包


* netstat -an | grep ESTABLISHED | awk -F " " '{print $5}' | cut -d ":" -f 1 | sort -nr


* top // 查看内存
* iotop // 查看io读写
* df -lh // 查看磁盘存储
* netstat -tunlp // 查看端口占用
* lsof -i // 查端口占用
* ps -aux | grep xx进程 // 查看关心的xx进程















































