
add_executable(lua lua.c)
target_link_libraries(lua liblua)

target_link_libraries(lua m)

target_include_directories(lua PUBLIC
	${LUA_HDR}
	)


install(TARGETS lua RUNTIME DESTINATION bin)
