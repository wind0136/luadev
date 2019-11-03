
add_executable(luac luac.c)
target_link_libraries(luac liblua)

target_link_libraries(luac m)

target_include_directories(luac PUBLIC
	${LUA_HDR}
	)

install(TARGETS luac RUNTIME DESTINATION bin)
