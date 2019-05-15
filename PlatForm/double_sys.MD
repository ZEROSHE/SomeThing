- 安装CUCKOO，但是无奈虚拟机嵌套虚拟机卡的要死，然而主要平台还是Win，所以不能重装成Ubuntu，所以想到双系统这个问题，整整装了一天

- 主要教程是按照http://www.cnblogs.com/Duane/p/5424218.html的教程操作，现在说一下我碰到的问题

- 分区按照这里不然GRUB会失败 https://www.jianshu.com/p/6925dcafeee6


- 启动之后手贱乱操作，最后发现只能进Ubuntu，不能进Windows

- 解决方法: 制作一块PE，然后选择修复就好，如果不可以，那我就没办法了，先把手头工作干了，以后在研究

- 启动Ubuntu不能联网，但Windows可以联网

- 解决方法: Windows模式先 我的电脑-->管理-->设备管理器-->网络适配器-->选择当前网卡-->属性-->电源管理-->去掉所有√，然后禁网，重启进入Ubuntu，看是否可以了

- ubuntu系统备份与还原
https://www.jianshu.com/p/968385ead4e5


- 显卡驱动安装（我这里敲了没有）
https://www.jianshu.com/p/9384af4896f3

- 磁盘空间分配
/ 30-50
/SWAP  16
/HOME 剩下的都给他

Cuckoo的安装
https://jiayu0x.com/2016/07/07/Cuckoo-install-config/ 
 
https://fl4g.cn/2018/06/06/Cuckoo-Sandbox%E5%AD%A6%E4%B9%A0-%E5%AE%89%E8%A3%85%E7%AF%87/ 

http://maofeichen.com/systemsecurity/2019/04/11/cuckoo-install-01.html 


删除无用空间

- 清理旧版本的软件缓存
sudo apt-get autoclean

- 清理所有软件缓存
sudo apt-get clean

- 删除系统不再使用的孤立软件
sudo apt-get autoremove

更新源
https://blog.csdn.net/zhangjiahao14/article/details/80554616 

https://blog.csdn.net/lxypeter521/article/details/81026365 

sudo apt-get update

sudo apt-get upgrade

source.list权限

644

777
