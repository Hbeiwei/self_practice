cmake_minimum_required(VERSION 3.16.3)
project(ModuleB)
# 获取当前目录想所有cpp文件
file(GLOB MODULE_B_SOURCES src/*.cpp)

# 创建静态库
add_library(ModuleB STATIC ${MODULE_B_SOURCES})

# 指定头文件路径
target_include_directories(ModuleB PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)



