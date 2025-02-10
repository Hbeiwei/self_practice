cmake_minimum_required(VERSION 3.16.3)
project(self_practice)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

#添加子模块
add_subdirectory(practice_0)
add_subdirectory(practice_1)

#生成可执行文件
add_executable(main main.cpp)

#链接子模块
target_link_libraries(main PUBLIC ModuleA ModuleB)

# 设置头文件路径
target_include_directories(main PUBLIC practice_0/include practice_0/include)

