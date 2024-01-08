cmake_minimum_required(VERSION 3.5)

project(template)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++20 -g -O0")
# print source dir
message("Source Dir is :  ${CMAKE_SOURCE_DIR}")
if(CMAKE_BUILD_TYPE STREQUAL "Debug")
    message("Debug Build")
    set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin/debug)
elseif(CMAKE_BUILD_TYPE STREQUAL "Release")
    message("Release Build")
    set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin/release)
endif()


file(GLOB SOURCES "src/*.*")

add_executable(exe1 ${SOURCES})