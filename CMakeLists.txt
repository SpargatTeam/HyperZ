cmake_minimum_required(VERSION 3.15)
project(HyperZ LANGUAGES C CXX)
set(CMAKE_CXX_STANDARD 23)
file(GLOB_RECURSE SOURCE
    ${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/src/*.c
)
add_library(${PROJECT_NAME} STATIC ${SOURCE})
include_directories(${CMAKE_SOURCE_DIR}/include)