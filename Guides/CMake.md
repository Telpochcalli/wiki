# CMake guide

In order for the following commands to run, you'll need to be on the project folder. 

## Basic steps:
1. Create a subdirectory with the name you'll identify the program.
2. Create a *CMakeLists.txt* file whithin the subdirectory.
3. On the document, add the following lines:
   1. cmake_minimum_required(VERSION 3.5.1)
   2. project(hello)
   3. add_executable(hello hello.cpp)
   
   4. set(CMAKE_SYSTEM_NAME Linux)
   5. set(CMAKE_SYSTEM_PROCESSOR arm)
   6. SET(CMAKE_CXX_FLAGS "--std=c++11")
   7. set(CMAKE_C_COMPILER /usr/bin/arm-linux-gnueabi-gcc)
   8. set(CMAKE_CXX_COMPILER /usr/bin/arm-linux-gnueabi-g++)
   9.  set(CMAKE_FIND_ROOT_PATH_MODE_PROGRAM NEVER)
   10. set(CMAKE_FIND_ROOT_PATH_MODE_LIBRARY ONLY)
   11. set(CMAKE_FIND_ROOT_PATH_MODE_INCLUDE ONLY)
   12. set(CMAKE_FIND_ROOT_PATH_MODE_PACKAGE ONLY)
4. Save 
5. Run CMake:
   1. mkdir build && cd build && cmake ..
6. Build the application:
   1. make

Comments: 
    The suggested way to cross compile code is by using [toolchains](https://cmake.org/cmake/help/v3.6/manual/cmake-toolchains.7.html). These predefine the necesarry rules needed for the platform.