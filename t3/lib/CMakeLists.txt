
message("CMAKE_SOURCE_DIR= ${CMAKE_SOURCE_DIR}")
message("CMAKE_BINARY_DIR= ${CMAKE_BINARY_DIR}")
set(LIB_SRC hello.c)

add_library(hello SHARED ${LIB_SRC})
add_library(hello_static STATIC ${LIB_SRC})
set_target_properties(hello_static PROPERTIES OUTPUT_NAME "hello")

set_target_properties(hello PROPERTIES VERSION 1.2 SONAME 1)

#set_target_properties(hello PROPERTIES CLEAN_DIRECT 1)
#set_target_properties(hello_static PROPERTIES CLEAN_DIRECT 1)

# Install
install(TARGETS hello hello_static
    LIBRARY DESTINATION lib
    ARCHIVE DESTINATION lib
    )

install(FILES hello.h DESTINATION include/hello)

