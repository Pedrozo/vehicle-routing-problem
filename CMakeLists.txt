cmake_minimum_required (VERSION 3.8)

project(VRP)

add_library(VRP_LIB src/vrp/foo.cpp)

target_include_directories(
    VRP_LIB
    PUBLIC
    inc/)

add_executable(DEMO demo/demo.cpp)

target_link_libraries(DEMO LINK_PUBLIC VRP_LIB)