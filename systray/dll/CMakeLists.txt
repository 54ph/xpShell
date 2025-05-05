cmake_minimum_required(VERSION 3.13)

project(stobject LANGUAGES CXX)

add_library(stobject SHARED
    access.c
    cfact.cpp
    csc.c
    dll.cpp
    hplug.c
    power.c
    print.cpp
    stobject.cpp
    systray.c
    systray.rc
    usbui.c
    volume.c
    windowsshell.manifest
)

target_precompile_headers(stobject
    PRIVATE
        cfact.h
        pccrdapi.h
        stclsid.h
        stdafx.h
        stobject.h
        stresid.h
        systray.h
        version.h
)

set_source_files_properties(WindowsApplication.rc
    PROPERTIES
        OBJECT_DEPENDS "${CMAKE_CURRENT_LIST_DIR}/*.ico"
)