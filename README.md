# qihoo-360-c301
qihoo360-c301固件


http://www.right.com.cn/forum/thread-209942-1-1.html
你刷的不是解密uboot的op固件，给你个教程！

1、准备好几个工具winscp、PuTTY、360最新的固件包、大神提供的openwrt的解锁uboot的固件包
    点链接下载：pan.baidu.com/s/1i3UDikP 密码：71wl

2、电脑网线接路由器，设置电脑网口为静态ip：192.168.1.2 子网掩码 255.255.255.0 其余为空

3、断开路由器电源，按住reset键，插上电源，等待黄色指示灯开始缓慢闪即可松开reset键。

4、电脑浏览器打开192.168.1.1， 出现上传rom页面

5、选择openwrt-r47884-ar71xx-generic-qihoo-c301-flash1-squashfs-factory.bin点击upload

6、重启后，打开wincsp软件，打开选择scp，输入主机名192.168.1.1端口默认，用户名 root 密码 admin ，点击登录

7、右侧找到并打开tmp文件夹（注意不是tmp/tmp），把uboot.bin文件复制到这里面。

8、打开putty软件，填上192.168.1.1，login as输入root

9、成功登陆进去后可以看到openwrt字样，这时候输入cd /tmp

10、然后输入 mtd -r write uboot.bin u-boot 路由会在3秒左右失去连接即是刷uboot成功，

11、等十几秒后拔掉电源，按住reset接通电源10秒左右松开，在电脑打开网页192.168.1.1就进入uboot了

注意全部搞完后，电脑网口还原成自动获取！

https://www.cnblogs.com/52fhy/p/5229078.html


http://downloads.openwrt.org/releases/18.06.1/targets/ar71xx/generic/
这两个刷一个就行，如果本身是op了，就用升级版，如果是原版，就用初始版
下载两个文件qihoo-c301-squashfs-factory.bin初始版
qihoo-c301-squashfs-sysupgrade.bin升级版


u-boot已经下载了，用winscp复制到对应位置，可以刷出来不死boot，看上面教程
