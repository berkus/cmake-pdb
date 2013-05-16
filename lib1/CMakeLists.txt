add_library(lib1 STATIC lib1.cpp $<TARGET_OBJECTS:lib2_internal>)
