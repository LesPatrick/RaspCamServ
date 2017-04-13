cmake_minimum_required(VERSION 3.6)
project(RaspCamServer)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -lraspicam -lmmal -lmmal_core -lmmal_util")

#find_package(raspicam REQUIRED)

# add libs
#include_directories(raspicam/src)
#add_subdirectory(raspicam)

# find and add sources
file(GLOB_RECURSE src_files "main.cpp")
add_executable(RaspCamServer ${src_files})
target_link_libraries(RaspCamServer ${raspicam_LIBS})
