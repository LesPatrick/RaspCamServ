cmake_minimum_required(VERSION 3.6)
project(RaspCamServer)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

# add libs
include_directories(raspicam/src)
add_subdirectory(raspicam)

# find and add sources
file(GLOB_RECURSE src_files "*.h" "*.cpp")
add_executable(RaspCamServer ${src_files})