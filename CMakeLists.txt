cmake_minimum_required(VERSION 3.1.0 FATAL_ERROR)
project(logging_utils CXX)

# Compilation options
set(ALWAYSON_CXX_FLAGS "--std=c++14 -Wall -Wextra $ENV{EXTRA_CXX_FLAGS}")
set(CMAKE_CXX_FLAGS "-O2 -g ${ALWAYSON_CXX_FLAGS}") # debug mode
message("-- INFO: Compiling in debug mode.\n-- INFO: flags are: " ${CMAKE_CXX_FLAGS})

include_directories("src")
include_directories("utils")

add_executable(all_tests "src/test.cpp")
