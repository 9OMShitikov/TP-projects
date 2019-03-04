cmake_minimum_required(VERSION 2.8)

project (print_square)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall")

execute_process(COMMAND python3 preparing.py WORKING_DIRECTORY A)

include_directories("B" "C" "./")

set (SOURCE "C/main.cpp")

add_executable(print_square ${SOURCE})

add_subdirectory(B)

target_link_libraries(print_square square_lib)
