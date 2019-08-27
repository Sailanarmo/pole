CMAKE_MINIMUM_REQUIRED(VERSION 3.0)

project(Pole)

set(CMAKE_CXX_STANDARD 11)

add_library(Poledump STATIC pole.cpp poledump.cpp)
