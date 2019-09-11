# https://www.cnblogs.com/wlzy/p/8214399.html
# https://blog.csdn.net/afei__/article/details/81201039
# https://blog.csdn.net/xh_hit/article/details/82917548

# cmake verson，指定cmake版本
cmake_minimum_required(VERSION 3.2)

# 设置项目名称
# 它会引入两个变量 libmf2_01_BINARY_DIR 和 libmf2_01_SOURCE_DIR，同时，cmake 自动定义了两个等价的变量 PROJECT_BINARY_DIR 和 PROJECT_SOURCE_DIR
project(mf-train)

# 指定编译类型，debug 或者为 release
# debug 版会生成相关调试信息，可以使用 GDB 进行
# release不会生成调试信息。当无法进行调试时查看此处是否设置为 debug
SET(CMAKE_BUILE_TYPE DEBUG)

# 指定编译器
# CMAKE_C_FLAGS_DEBUG            ----  C 编译器
# CMAKE_CXX_FLAGS_DEBUG        ----  C++ 编译器
# -g：只是编译器，在编译的时候，产生调试信息。
# -Wall：生成所有警告信息。一下是具体的选项，可以单独使用
# CXXFLAGS = -Wall -O3 -pthread -std=c++0x -march=native
# CXXFLAGS = -Wall -g -pthread -std=c++0x -march=native
SET(CMAKE_CXX_FLAGS_DEBUG "-Wall -g -pthread -std=c++0x -march=native")

add_executable(mf-train mf-train.cpp mf.cpp mf.h mf.def)  #制定生成目标




