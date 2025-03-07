# 树莓派4安装ubuntu系统
- 下载Raspberry Pi Imager
```C
https://downloads.raspberrypi.org/imager/imager_latest.exe
```
- 下载并安装putty
```C
https://www.putty.be/latest.html
```
- 电脑插入TF卡
- Raspberry Pi Imager烧录器配置如下：  
![配置](https://github.com/fortunate-ouyanghui/env-config/blob/main/raspberry1.jpg)
![配置](https://github.com/fortunate-ouyanghui/env-config/blob/main/raspberry2.jpg)
![配置](https://github.com/fortunate-ouyanghui/env-config/blob/main/raspberry3.jpg)
- 烧录
- 使用Putty连接树莓派Ubuntu系统
- 输入账号和密码

- 更新Ubuntu系统
```C
sudo apt update
sudo apt upgrade
```
- 安装gnome桌面
```C
sudo apt install ubuntu-gnome-desktop
```
- 安装远程桌面服务
```C
#1、安装远程桌面服务xrdp：
sudo apt-get install xrdp
#2、可以忽略此步：配置xrdp服务，开启3390端口，默认配置3389改为3390。
sudo sed -i 's/port=3389/port=3390/g' /etc/xrdp/xrdp.ini
#3、可以忽略此步：如果执行了上面的2，则需要重启xrdp服务。
sudo service xrdp restart
```


