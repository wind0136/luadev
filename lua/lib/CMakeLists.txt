
set(SRC 
    lapi.c lbitlib.c lctype.c  ldo.c    lgc.c     
    llex.c      loadlib.c   loslib.c   lstring.c  
    ltablib.c     lvm.c lauxlib.c   lcode.c     
    ldblib.c  ldump.c  linit.c   lmathlib.c  
    lobject.c   lparser.c  lstrlib.c  ltm.c      
    lundump.c   lzio.c lbaselib.c  lcorolib.c  
    ldebug.c  lfunc.c  liolib.c  lmem.c      
    lopcodes.c  lstate.c   ltable.c lutf8lib.c  
)

add_library(liblua STATIC ${SRC})

target_include_directories(liblua PUBLIC ${LUA_HDR})


set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fPIC")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fPIC")

install(TARGETS liblua
	RUNTIME DESTINATION bin
	LIBRARY DESTINATION lib
	ARCHIVE DESTINATION lib)

install(TARGETS liblua
	RUNTIME DESTINATION bin
	LIBRARY DESTINATION lib
	ARCHIVE DESTINATION lib)
