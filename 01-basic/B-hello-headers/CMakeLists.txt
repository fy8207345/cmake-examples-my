cmake_minimum_required(VERSION 3.5)

project(hello-headers)

# 创建一个变量，把所有的cpp文件关联起来
set(SOURCES
	src/Hello.cpp
	src/main.cpp
	)

add_executable(${PROJECT_NAME} ${SOURCES})
# 必须写在add_executable后面？？
#头文件所在的目录， PRIVATE表示作用域
target_include_directories(${PROJECT_NAME}
	PRIVATE
	${PROJECT_SOURCE_DIR}/include
	)
