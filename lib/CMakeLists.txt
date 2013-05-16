cmake_minimum_required(VERSION 2.8.10)
project(outerlib)

add_library(innerlib_internal OBJECT lib2.cpp)
add_library(innerlib STATIC $<TARGET_OBJECTS:innerlib_internal>)
add_library(outerlib STATIC lib1.cpp $<TARGET_OBJECTS:innerlib_internal>)

install(TARGETS outerlib 
        DESTINATION ${CMAKE_BINARY_DIR}/../outerlib/)
install(FILES ${CMAKE_BINARY_DIR}/${BUILD_TYPE}/outerlib.pdb
        DESTINATION ${CMAKE_BINARY_DIR}/../outerlib/)
