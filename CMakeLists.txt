cmake_minimum_required(VERSION 3.10)
project(MyProject)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(myapp main.cpp)

# Для Windows
if(WIN32)
    target_compile_options(myapp PRIVATE /W4 /WX)
else()
    target_compile_options(myapp PRIVATE -Wall -Wextra -Wpedantic)
endif()