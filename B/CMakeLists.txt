cmake_minimum_required(VERSION 2.8)

project(square_lib)

set(SOURCE_LIB lib.cpp)

set(HEADER_LIB lib.h)

add_library(square_lib STATIC ${SOURCE_LIB} ${HEADER_LIB})
