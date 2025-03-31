- 创建环境
```
conda create -n ENV_NAME python=3.9
```
- 激活环境
```C
conda activate ENV_NAME
```
- 退出环境
```C
conda deactivate
```
- 查看当前存在的环境
```C
conda env list
```
- 安装conda后，每次启动终端都会默认进入base虚拟环境，要想取消执行该命令
```C
conda config --set auto_activate_base false
```
- 删除环境
```C
conda remove ENV_NAME -all
```
