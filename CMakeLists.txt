cmake_minimum_required(VERSION 3.5)
project(mdnsd)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
include_directories(mdnsd)

set(SOURCE_FILES   mdnsd/mdnsd.c
        mdnsd/control.c
        mdnsd/interface.c
        mdnsd/kiface.c
        mdnsd/log.c
        mdnsd/mdns.c
        mdnsd/packet.c
        )

add_executable(mdnsd ${SOURCE_FILES})

# target_link_libraries(light_bulb libpthread.so)