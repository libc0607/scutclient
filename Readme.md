scutclient
=================

背景
--------

编译校园网客户端到OpenWrt中  
这个是Fork了[这里](https://github.com/scutclient/scutclient)   

编译方法
--------

下载Makefile--OpenWrt, 重命名为Makefile放在package/scutclient中（没有该scutclient文件夹的话就自己新建一个）  
运行make menuconfig后，在Network中可以找到scutclient  
选择*编译，根据提示选择是否集成LuCI    
最后保存退出后，可以运行make package/scutclient/compile V=s进行编译scutclient  
ipk包会出现在Openwrt编译根目录的bin文件夹中  
可能报错原因：configure无执行权限  
PKG_SOURCE_VERSION自行改为最近的commit id  
