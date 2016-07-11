cmake_minimum_required(VERSION 2.8)

project(dloadtool)

#src for dloadtool
set(SRC util.c
	dload.c
	mbn.c
	ihex.c
	main.c)

# dtloadtool
add_executable(dloadtool ${SRC})

#subdirs
add_subdirectory(libcintelhex)


# includes
include_directories(${PROJECT_SOURCE_DIR}/libcintelhex/include
		${PROJECT_SOURCE_DIR}
)

target_link_libraries(dloadtool cintelhex)


