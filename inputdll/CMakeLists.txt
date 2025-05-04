cmake_minimum_required(VERSION 3.13)

project(inputdll)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 11)

# Add the source files to the project
set(SOURCE_FILES
    advanced.c
    cicutil.c
    external.c
    input.c
    input.manifest
    input.rc
    inputdlg.c
    regdlg.c
    util.c
)

# Add the header files to the project
set(HEADER_FILES
    external.h
    input.h
    inputdlg.h
    inputhlp.h
    resource.h
    util.h
)

# Create the shared library (DLL)
add_library(input SHARED ${HEADER_FILES} ${SOURCE_FILES})