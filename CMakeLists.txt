cmake_minimum_required(VERSION 3.20)

project(xpShell)

# Write properties that are influenced by the toolchain
#
message(STATUS "CMAKE_CROSSCOMPILING = ${CMAKE_CROSSCOMPILING}")
message(STATUS "CMAKE_SYSTEM_NAME = ${CMAKE_SYSTEM_NAME}")
message(STATUS "CMAKE_SYSTEM_PROCESSOR = ${CMAKE_SYSTEM_PROCESSOR}")
message(STATUS "MSVC_TOOLSET_VERSION = ${MSVC_TOOLSET_VERSION}")
message(STATUS "MSVC_VERSION = ${MSVC_VERSION}")

# Demonstrate that toolchain-related tooling can be found
#
find_program(NMAKE_PATH
    nmake.exe
)

message(STATUS "NMAKE_PATH = ${NMAKE_PATH}")

# Build a set of representative projects
#
add_compile_definitions(
    UNICODE
    _UNICODE
)

include_directories(include)

add_subdirectory(inputdll)
add_subdirectory(sndvol32)
add_subdirectory(systray)