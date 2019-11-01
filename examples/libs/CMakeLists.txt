include_directories(${LUA_HDR})

add_library(lib1 SHARED lib1.c)
target_link_libraries(lib1 liblua)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fPIC")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fPIC")
