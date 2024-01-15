cmake_minimum_required(VERSION 3.10)
project(demo)

# 指定C++标准
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# 查找GLFW库
find_package(glfw3 REQUIRED)

# 添加包含GLAD的可执行文件
add_executable(demo main.cpp external/glad.c)

# 包含GLAD头文件的目录
include_directories(/usr/local/include)

# 链接GLFW库
target_link_libraries(demo glfw)
