# 实验7 UDP实验
## 一、实验目的

1. 掌握Linux下UDP的通信原理与实现。
2. 熟悉Linux下的socket函数编程方法。
## 二、实验内容
交叉编译UDP协议文件，将编译后的文件通过NFS服务器下载至开发板运行。
## 三、实验步骤

1. 编译文件
将D盘中“05-实验例程/第12章”的“12.8-udp”文件夹复制到D盘Windows和Linux共享文件夹“forlinux”，然后将listener和utalker两个文件夹中的文件分别完成交叉编译。
2. 设置NFS服务
1）建立一个NFS服务的专有文件夹nfs。
```sh
$ sudo mkdir /opt/nfs
```
2）编辑exports文件。
```sh
$ gedit /etc/exports
```
在文件的最后一行添加：`/opt/nfs *(rw,sync,no_root_squash)`
3）重启portmap服务。
```sh
$ sudo /etc/init.d/portmap restart
```
4）重启nfs服务。
```sh
$ sudo /etc/init.d/nfs-kernel-server restart
```
5）显示nfs共享目录。
```sh
$ showmount -e 
````
3. 运行文件
1）正确设置网络，确保Linux系统与开发板之间能互相ping通。
2）利用Serial COM2串口工具在开发板上挂载NFS服务。
```sh
# mount -t nfs 192.168.70.**:/opt/nfs  /tmp -o intr,nolock,rsize=1024,wsize=1024
```
注意：命令中的192.168.70.**为Linux系统的IP地址。
3）进入开发板tmp文件夹确认存在listener和talker，修改权限后运行文件。
```sh
# cd /tmp
# ls
# chmod 777 listener
# ./listener
# chmod 777 talker
# ./talker
```
## 四、实验报告
1. 附主要步骤中的命令及其结果截图。
2. 归纳总结本实验。
