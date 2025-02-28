cmake_minimum_required(VERSION 3.0)
project(HyperZ VERSION 10000z LANGUAGES C CXX)
file(GLOB_RECURSE SOURCE
    ${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/src/*.c
)
if (ANDROID)
    add_library(${PROJECT_NAME} SHARED ${SOURCE})
else()
    add_executable(${PROJECT_NAME} ${SOURCE})
endif()
include_directories(${CMAKE_SOURCE_DIR}/source)