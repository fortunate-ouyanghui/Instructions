## 安装依赖环境
```C
sudo apt-get install build-essential libgtk2.0-dev libavcodec-dev libavformat-dev libjpeg-dev libswscale-dev libtiff5-dev
sudo apt-get install libgtk2.0-dev
sudo apt-get install pkg-config
```
## 下载opencv
请选择合适的版本:https://opencv.org/releases/
## 将下载好的文件命名为opencv4
## 编译和安装
```C
cd opencv4
mkdir build
cd build
sudo make -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local ..
sudo make -j4
sudo make install
```
