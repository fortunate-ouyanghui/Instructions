- conda新建环境
```C
conda create --name EDC_env python=3.8
删除环境变量
conda remove --name myenv --all
```
- 激活环境
```C
conda activate EDC_env
```
- 安装依赖库
```C
conda install -y opencv-python=3.4.17.63 -c conda-forge
conda install -y pybind11 cmake
pip install maixpy3==0.5.3
pip install pyserial
```
