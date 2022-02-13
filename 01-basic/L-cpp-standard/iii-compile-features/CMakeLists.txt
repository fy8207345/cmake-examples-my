# Set the minimum version of CMake that can be used
# To find the cmake version run
# $ cmake --version
cmake_minimum_required(VERSION 3.1)

# Set the project name
project (hello_cpp11)

add_executable(hello_cpp11 main.cpp)

target_compile_features(hello_cpp11 PUBLIC cxx_auto_type)

message("List of compile features : ${CMAKE_CXX_COMPILE_FEATURES}")
