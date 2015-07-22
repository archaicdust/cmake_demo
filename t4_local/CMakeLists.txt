#cmake_minimum_required(VERSION 2.8)

project(HELLO)

message("CMAKE_SOURCE_DIR= ${CMAKE_SOURCE_DIR}")
message("CMAKE_BINARY_DIR= ${CMAKE_BINARY_DIR}")

add_subdirectory(lib)
add_subdirectory(src)
