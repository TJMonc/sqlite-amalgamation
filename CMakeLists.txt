cmake_minimum_required(VERSION 3.21)
add_definitions(-std=c17 -std=c++20 -O3)

project(sqlite3)
set(BUILD_SHARED_LIBS ON)
file(GLOB SOURCES "src/*.c")

target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_SOURCE_DIR}/include/sqlite3.h)
set(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)
add_library(${PROJECT_NAME} ${SOURCES})
