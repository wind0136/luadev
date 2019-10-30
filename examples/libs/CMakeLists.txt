include_directories(${LUAROOT})

add_library(lib1 SHARED lib1.c)
target_link_libraries(lib1 liblua)