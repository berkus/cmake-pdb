project(cmake-pdb)

add_library(lib2_internal OBJECT lib2.cpp)
add_library(lib2 STATIC $<TARGET_OBJECTS:lib2>)
add_library(lib1 STATIC lib1.cpp $<TARGET_OBJECTS:lib2_internal>)

add_executable(test test.cpp)
target_link_libraries(test lib1)
