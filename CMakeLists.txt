cmake_minimum_required(VERSION 3.8)
project(hosts)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_VERBOSE_MAKEFILE ON)

set(SOURCE_FILES
        tool.cpp
        tool.rc)

add_executable(tools ${SOURCE_FILES})
target_link_libraries(tools wininet)

set(OBJECT_SOURCE_CODE
        object-runwithcode/choose.cpp
        object-runwithcode/choose.rc)

add_executable(choose ${OBJECT_SOURCE_CODE})

