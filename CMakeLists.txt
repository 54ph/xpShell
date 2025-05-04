cmake_minimum_required(VERSION 3.13)

project(xpShell)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 11)

include_directories(include)

add_subdirectory(systray)
add_subdirectory(inputdll)
add_subdirectory(sndvol32)