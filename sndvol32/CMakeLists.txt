cmake_minimum_required(VERSION 3.13)

project(sndvol32)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 11)

# Add the source files to the project
set(SOURCE_FILES
    choice.c
    dlg.c
    mixer.c
    nonmixer.c
    pvcd.c
    reg.c
    sndvol32.manifest
    sndvol32.rcv
    utils.c
    volume.c
    volume.rc
    vu.c
)

# Add the header files to the project
set(HEADER_FILES
    dlg.h
    helpids.h
    pvcd.h
    utils.h
    volids.h
    volumei.h
    vu.h
)

# Create the shared library (DLL)
add_executable(sndvol32 SHARED ${HEADER_FILES} ${SOURCE_FILES})