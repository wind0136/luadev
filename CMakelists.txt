cmake_minimum_required(VERSION 3.6)
project(lua)

set (CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/CMake/Modules)

set (LUAROOT ${CMAKE_SOURCE_DIR}/src)

add_subdirectory(src)
add_subdirectory(test)
