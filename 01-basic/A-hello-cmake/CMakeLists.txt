#本项目的Cmake最低版本要求
cmake_minimum_required(VERSION 3.5)
# 指定项目名称, 会生成一个${PROJECT_NAME}的变量
project(hello_cmake)
# 生成一个可执行文件，第一个参数是可执行文件的名称
# 后面的参数是参与该文件构建的源文件
add_executable(hello_cmake main.cpp)
# add_executable(${PROJECT_NAME} main.cpp) 与上面等价
