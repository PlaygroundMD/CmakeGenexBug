file(WRITE file.cpp "")
add_library(SubLib STATIC file.cpp)
target_link_libraries(MainLib PUBLIC SubLib)
