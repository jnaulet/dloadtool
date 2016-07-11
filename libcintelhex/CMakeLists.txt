# project config
cmake_minimum_required(VERSION 2.8)
project(cintelhex)

# cintelhex
add_library(cintelhex STATIC
	src/ihex_copy.c
	src/ihex_parse.c
	src/ihex_record.c )

include_directories(${PROJECT_SOURCE_DIR}/include)

set(CMAKE_C_FLAGS "-std=c99")
