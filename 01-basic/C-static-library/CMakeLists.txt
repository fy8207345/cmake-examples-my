cmake_minimum_required(VERSION 3.5)

project(hello_library)

# 编译生成一个静态库
add_library(hello_library STATIC
	src/Hello.cpp
	)

# 编译这个静态库时会使用到这个include目录
# 任意编译目标引用该静态库时，也会使用这个include目录
target_include_directories(hello_library
	PUBLIC
	${PROJECT_SOURCE_DIR}/include
	)

add_executable(hello_binary
	src/main.cpp
	)

target_link_libraries(hello_binary
	PRIVATE
	hello_library
	)
