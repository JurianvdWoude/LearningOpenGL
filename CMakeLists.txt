
cmake_minimum_required(VERSION 3.10)
project(LearnOpenGL)
#file(GLOB_RECURSE SOURCE_FILES
#       ./src/*.c
#       ./src/*.cpp)
#file(GLOB_RECURSE HEADER_FILES
#       ./include/**/*.h)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_DEBUG "${CMAKE_SOURCE_DIR}/build/debug")
# Use cmake --help-policy ... to check 
# set(CMAKE_POLICY_DEFAULT_CMP0072 NEW)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
include_directories(./include/)
add_library(Glad ./src/glad.c)

add_executable(exe src/main.cpp)

target_link_libraries(exe OpenGL)
target_link_libraries(exe glfw)
target_link_libraries(exe Glad)

target_compile_options(exe PRIVATE -Wall)

