
add_subdirectory(lib)
add_subdirectory(lua)
add_subdirectory(luac)

file(GLOB LUAHDR "includes/*")
install(FILES ${LUAHDR}
	DESTINATION includes)
