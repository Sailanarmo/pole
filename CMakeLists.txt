CMAKE_MINIMUM_REQUIRED(VERSION 3.0)

project(Pole)

set(CMAKE_CXX_STANDARD 11)

if(MINGW)
  set(Boost_LIBRARY_DIRS ${Boost_LIBRARY_DIR})

  include_directories(${Boost_INCLUDE_DIRS})
  add_library(Poledump STATIC pole.cpp poledump.cpp)
  #add_dependencies(Poledump Boost_external_download)
  target_link_libraries(Poledump ${Boost_LIBRARIES})

  message(STATUS ${Boost_INCLUDE_DIRS})
else()
  add_library(Poledump STATIC pole.cpp poledump.cpp)
endif()
