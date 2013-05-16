add_library(lib2_internal OBJECT lib2.cpp)
add_library(lib2 STATIC $<TARGET_OBJECTS:lib2_internal>)
