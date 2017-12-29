project(Spartan C)

set(sds_SRCS sds.c sds.h sdsalloc.h)

add_library(sds STATIC ${sds_SRCS})

set_property(TARGET sds PROPERTY C_STANDARD 99)
set_property(TARGET sds PROPERTY C_STANDARD_REQUIRED ON)

find_path(sds_INCLUDE_DIR sds.h ${CMAKE_CURRENT_LIST_DIR})
