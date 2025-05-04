# Add the source files to the project
set(SOURCE_FILES
	systray.c
	systray.rc
	systray.def
)

# Add the header files to the project
set(HEADER_FILES
	version.h
)

add_executable(systray WIN32 ${HEADER_FILES} ${SOURCE_FILES})