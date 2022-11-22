cmake_minimum_required(VERSION 3.15)

project(myproject LANGUAGES CXX)

# set the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# lib
add_library(mylib)

target_sources(mylib PRIVATE
    src/lib.cpp
)

target_include_directories(mylib PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/inc
)

# configure and build gtest
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
set(BUILD_GMOCK OFF CACHE BOOL "" FORCE)
add_subdirectory(googletest)

# test
add_subdirectory(test)