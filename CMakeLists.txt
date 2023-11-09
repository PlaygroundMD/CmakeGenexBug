cmake_minimum_required(VERSION 3.10.0)
project(Test)

file(WRITE file.cpp "")
add_library(MainLib STATIC file.cpp)

add_subdirectory(subdir)

file(GENERATE OUTPUT output$<CONFIG>.txt CONTENT "$<TARGET_PROPERTY:MainLib,LINK_LIBRARIES>")
