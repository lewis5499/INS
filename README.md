# INS

## 1.程序编译与运行

### 1.1 源码

项目完全采用CMake管理，CMakeLists.txt保存了项目配置信息(x64)。
项目采用MinGW64的g++编译，./src目录下提供了所有源码，包含C++和matlab两部分。
其中，(.m)文件为粗对准、可视化评估推算轨迹、误差的matlab脚本文件，代码可直接运行，运行时调用的(.mat)文件位于./dataset文件夹中。

### 1.2 依赖库

除了基本的C++标准库之外，INS项目依赖Eigen库。

### 1.3 运行结果

运行测试数据(demo)、小推车数据的中间结果(A15)、解算结果以及绘图等结果均保存至./outfiles/对应文件夹中。

## 2 数据集

### 2.1 测试数据

./dataset/01 demo/为解算测试的示例数据。
./dataset/02 A15/为自采小推车数据（小推车与POS-A15型IMU捷联）。

### 2.2 可视化评估数据

纯INS推算的各类结果已打包为(.mat)文件，在./dataset文件夹内。

### 2.3 GNSS/INS松组合参考数据

此数据在./dataset/03 ref/内，组合导航的解算结果是基于./dataset/02 A15/的自采小推车数据。