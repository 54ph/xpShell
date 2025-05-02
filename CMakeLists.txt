cmake_minimum_required(VERSION 3.13)

project(xpShell)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 11)

include_directories(${WINDOWS_SDK_INCLUDE_DIR}) 

add_subdirectory(systray)