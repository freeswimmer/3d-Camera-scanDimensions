cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(pclBox)

find_package(PCL 1.7 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
include_directories("/usr/include/ni/")
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (pclBox pclBox.cpp tools.cpp)
target_link_libraries (pclBox ${PCL_LIBRARIES})
