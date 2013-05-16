project(outerlib)

add_library(innerlib_internal OBJECT lib2.cpp)
add_library(innerlib STATIC $<TARGET_OBJECTS:innerlib_internal>)
add_library(outerlib STATIC lib1.cpp $<TARGET_OBJECTS:innerlib_internal>)
