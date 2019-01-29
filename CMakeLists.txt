
cmake_minimum_required (VERSION 2.6)
project (json-parser)

set (CMAKE_C_FLAGS "-std=c89 -ansi -pedantic -Wall ${CMAKE_C_FLAGS}")

set (SOURCES ${SOURCES} json.c json.h)

add_library (jsonparser ${SOURCES})

set_target_properties (jsonparser PROPERTIES VERSION 0.1.0
                                              SOVERSION 0.1)

target_link_libraries (jsonparser ${LIBS})

install (TARGETS jsonparser DESTINATION lib)
install (FILES json.h DESTINATION include)


