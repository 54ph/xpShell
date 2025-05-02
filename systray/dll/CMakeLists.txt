cmake_minimum_required(VERSION 3.13)

project(stobject)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 11)

# Add the source files to the project
set(SOURCE_FILES
    access.c
    cfact.cpp
    csc.c
    hplug.c
    power.c
    print.cpp
    stobject.cpp
    systray.c
    usbui.c
    volume.c
    windowsshell.manifest
)

# Add the header files to the project
set(HEADER_FILES
    cfact.h
    pccrdapi.h
    stclsid.h
    stdafx.h
    stobject.h
    stresid.h
    version.h
)

# Create the shared library (DLL)
add_library(stobject SHARED ${HEADER_FILES} ${SOURCE_FILES})