cmake_minimum_required(VERSION 2.8.10)
project(exe)

add_executable(test test.cpp)

find_library(OUTERLIB outerlib PATHS ${CMAKE_BINARY_DIR}/../outerlib/)
target_link_libraries(test ${OUTERLIB})
