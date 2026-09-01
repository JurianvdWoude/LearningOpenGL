cmake_minimum_required(VERSION 3.10)

project(LearnOpenGL LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

add_library(Glad src/glad.c)

target_include_directories(Glad PUBLIC
    ${CMAKE_SOURCE_DIR}/include
)

add_executable(LearnOpenGL
    src/main.cpp
)

target_link_libraries(LearnOpenGL PRIVATE
    Glad
    glfw
    OpenGL::GL
)

target_compile_options(LearnOpenGL PRIVATE
    -Wall
)
