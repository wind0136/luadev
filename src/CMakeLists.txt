
set(LIBLUA_SRC 
    lapi.c      lbitlib.c   
    lctype.c  ldo.c    lgc.c     
    llex.c      loadlib.c   
    loslib.c   lstring.c  
    ltablib.c     
    lvm.c
    lauxlib.c   lcode.c     ldblib.c  
    ldump.c  linit.c   
    lmathlib.c  lobject.c   lparser.c  
    lstrlib.c  ltm.c      lundump.c   lzio.c
    lbaselib.c  lcorolib.c  ldebug.c  
    lfunc.c  liolib.c  
    lmem.c      lopcodes.c  lstate.c   
    ltable.c 
    lutf8lib.c  
)

add_library(liblua STATIC ${LIBLUA_SRC})

add_executable(lua lua.c)
target_link_libraries(lua liblua)


add_executable(luac luac.c)
target_link_libraries(luac liblua)