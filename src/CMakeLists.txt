#AUX_SOURCE_DIRECTORY (. SRC_LIST)	# 把当前目录下的源文件存列表存放到变量SRC_LIST里,但是是所有文件，为避免将不需要的文件一起编译，用set更好
set( SRC_LIST
	 ./main.cpp)  

INCLUDE_DIRECTORIES (../include)	# 用来向工程添加多个指定头文件的搜索路径，路径之间用空格分隔

ADD_EXECUTABLE (main ${SRC_LIST})	#表示最终要生成的elf文件的名字叫main，使用的源文件是main.cpp

# EXECUTABLE_OUT_PATH和PROJECT_SOURCE_DIR是CMake自带的预定义变量，其意义如下，
#1. EXECUTABLE_OUTPUT_PATH ：目标二进制可执行文件的存放位置 
#2. PROJECT_SOURCE_DIR：工程的根目录
SET (EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)	
