- 具体使用请看env-config项目code分支下的socket
## 配置路径
- set(变量名 变量初始值 声明为cache缓存变量 变量类型 描述)
```C
set(INCLUDE_DIR "{CMAKE_CURRENT_SOURCE_DIR}/include" CACHE PATH "这是头文件目录")
```
## 打印消息
- message(类型 消息)
```C
message(STATUS "头文件目录:"${INCLUDE_DIR})
```
## 编译配置
```C
set(CMAKE_CXX_STANDARD 17)
```
## 包含头文件路径
```C
add_library(global INTERFACE)
target_include_directories(
  global
  INTERFACE
  ${INCLUDE_DIR}
)
```
## 配置可执行文件
```C
add_executable(cli
  ${SRC_DIR}/client.cpp
)
```
## 统一设置输出目录
```C
set_target_properties(cli PROPERTIES
  RUNTIME_OUTPUT_DIRECTORY ${BIN_OUTPUT_DIR}
)
```
## 配置依赖
```C
target_link_libraries(cli PRIVATE global)
```





