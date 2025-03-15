# 配置openvino
- 环境：ubuntu22
- 步骤：  
1. 在opt目录下新建intel文件夹 
```C
sudo mkdir /opt/intel
```
2. 下载openvino包
```C
curl -L https://storage.openvinotoolkit.org/repositories/openvino/packages/2024.5/linux/l_openvino_toolkit_ubuntu22_2024.5.0.17288.7975fa5da0c_x86_64.tgz --output openvino_2024.5.0.tgz
```
3. 解压
```C
tar -xf openvino_2024.5.0.tgz
```
4. 将包移动到指定目录下
```C
sudo mv l_openvino_toolkit_ubuntu22_2024.5.0.17288.7975fa5da0c_x86_64 /opt/intel/openvino_2024.5.0
```
5. 进入
```C
cd /opt/intel/openvino_2024.5.0
```
6. 编译
```C
sudo -E ./install_dependencies/install_openvino_dependencies.sh
```
7. 每次打开终端，openvino环境自动初始化  
  7.1. 主目录中ctrl+h,找到 .bashrc文本文件  
  7.2. 添加  
  ```C
  #openvino init
  source /opt/intel/openvino_2024.5.0/setupvars.sh
  ```

      
