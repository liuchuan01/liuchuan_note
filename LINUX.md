# LINUX

课程规划：基础篇，实际操作篇，高级篇，java定制篇，大数据定制篇，python定制篇，企业面试篇

学习阶段：基本操作命令，linux配置，linux开发环境配置，基本shell脚本，安全设置，理解linux内核   、

<img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h4feeo9t9mj20qo0dm76p.jpg" alt="截屏2022-07-22 上午8.27.50" style="zoom:50%;" />

虚拟机网络：

1. 桥接模式，虚拟系统直接分配ip，可以与外部通讯，容易ip冲突 

2. NAT模式（网络地址转换模式），物理机代理虚拟系统ip，也可以与外部通讯，虚拟系统使用的IP，与物理机不在同一网段，避免冲突
3. 主机模式，独立配置，与外部无关

## 一.目录结构

linux文件系统采用级层式树状目录。

> 在Linux的世界里，一切皆文件

==pwd==显示当前所在目录

主要目录：

1. /      根目录

2. /bin （binary） 存放着常用的命令

3. /sbin （super user binary） 系统管理员使用的系统管理程序

4. /home 下分用户文件夹

5. /root 系统管理员主目录

6. /lib 系统开机所需要最基本的动态连接共享库
7. /etc 所有系统管理所需要的配置文件，如各类.conf
8. /usr 存放用户安装的应用程序与文件
9. /boot 启动Linux时的核心文件，连接文件
10. /proc 虚拟目录，系统内存的映射
11. /srv （service） 存放服务启动后需要提取的数据
12. /sys 存放linux2.6版本之后新出现的文件系统sysfs
13. /tmp 存放临时文件
14. /dev 把所以的设备作为文件管理
15. /media 如u盘，光驱被linux识别后挂载于此 
16. /mnt 临时挂载文件系统
17. /var 存放不断变化的东西，例如日志

## 二.远程登录

在开发时，往往多个用户共享一个Linux主机，通过远程登录进行项目管理开发

一般使用Xshell（远程登录），Xftp（远程文件传输）

连接时使用公网IP，

可使用ping进行检测，是否能连通



## 三.开机/重启，用户登录/注销

关机/重启指令：

+ shutdown -h后跟参数“now”/“1”

  h是halt的缩写

+ shutdown -r后跟参数“now”/“1”

  r是reboot

+ sync（将内存数据同步到磁盘，现在的关机指令中已包含）

+ halt/reboot也可直接输入使用

用户登录/注销

+ logout

  注销（仅在无图形界面有效）

## 四.用户管理

1. 添加用户

   + useradd name

     默认该用户家目录在home下

     且名称与用户名相同

   + useradd -d /home/dpath/ name

     指定该用户家目录地址以及名称

2. 设置密码

   + passwd

     给当前用户设置密码

   + passwd name

     给指定用户切换密码

3. 删除用户

   + userdel name

     仅删除用户但不删除家目录

   + userdel -r name

     删除用户及家目录

4. 查询用户

   + id name

     查询用户信息

   + who am i

   + 查询当前登录身份

5. 切换用户

   + su - name

     高权限用户转到低权限不需要密码

     反之需要

   

## 五.运行级别

0关机

1单用户（找回丢失密码）

2多用户但无网络

3多用户有网络（最常用）

4系统未使用保留给用户

5图形界面（开机默认）

6系统重启

### init命令

init x进入x状态

### 查看当前系统启动级别

systemctl get-default

改变系统启动级别

systemctl set-default multi-user.target

> multi-user.target  相当于3级
>
> graphical.target   相当于5级

## 六.文件目录指令

### man

*用于展示命令的用法*

==man+文件名/指令名==

显示指令参数/用法/选项

### pwd

*列出当前绝对路径*

==pwd==

### cd

*切换目录*

==cd 文件夹==

进入文件夹

==cd ～==

回到家目录（当前用户）

==cd ..==

返回上一级
