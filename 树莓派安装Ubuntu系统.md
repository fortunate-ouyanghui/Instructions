# 树莓派3B安装ubuntu系统
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
1. 选择ubuntu系统
![1](https://github.com/user-attachments/assets/c78d4c76-1900-4550-b8a4-c88db5daf2d3)
2. 开启SSH服务
![2](https://github.com/user-attachments/assets/616cc2e0-9ad6-40e6-a849-e0078b838836)
3. 配置热点
![3](https://github.com/user-attachments/assets/ee5022a7-8be1-4284-b1b7-079d032ce42d)
- 烧录
- 使用Putty连接树莓派Ubuntu系统
1. 获取树莓派ip
![4](https://github.com/user-attachments/assets/3ceb230d-bb67-452f-9d2e-af41c1fc3971)
2. 连接
![5](https://github.com/user-attachments/assets/13b29d00-98ad-42be-a36b-56be6b9046fe)
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


