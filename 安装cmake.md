# 配置cmake
- 环境：ubuntu22
- 步骤：
0. 安装编译器
```C
sudo apt update
sudo apt install build-essential
#临时设置环境变量
export CC=/usr/bin/gcc
#永久设置环境变量
echo 'export CC=/usr/bin/gcc' >> ~/.bashrc
source ~/.bashrc
```
1. 下载cmake
```C
https://github.com/Kitware/CMake/releases/download/v3.24.2/cmake-3.24.2.tar.gz
```
2. 解压
```C
tar -zxvf cmake-3.24.2.tar.gz
```
3. 进入
```C
cd cmake-3.24.2
```
4. 执行
```C
./bootstrap
```
5. 编译
```C
make
```
6. 安装
```C
sudo make install
```
7. 查看cmake版本
```C
cmake --version
```
