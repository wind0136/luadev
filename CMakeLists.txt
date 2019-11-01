cmake_minimum_required(VERSION 3.6)
project(lua)

set (CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/CMake/Modules)

set (LUA     ${CMAKE_SOURCE_DIR}/lua)
set (LUA_HDR ${LUA}/includes)

add_subdirectory(lua)
add_subdirectory(examples)

install(DIRECTORY examples/ DESTINATION share/examples)
