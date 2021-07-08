# 最低版本号
cmake_minimum_required( VERSION 3.15 )
# 项目名称
project( cpp_primer )
# 源文件
set( SOURCES
  src/main.cpp
)

# 编译参数
add_compile_options( -Wall -std=c++2a)

# 可执行文件
add_executable( ${PROJECT_NAME} ${SOURCES} )
# 头文件
target_include_directories( ${PROJECT_NAME}
  PRIVATE
    ${PROJECT_SOURCE_DIR}/include
)
# 输出到build/bin
set_target_properties( ${PROJECT_NAME}
  PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/bin
)
