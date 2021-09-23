cmake_minimum_required(VERSION 3.5 FATAL_ERROR)
add_definitions(-std=c++14)

project(cluster_extraction)

find_package(PCL 1.7.2 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (cluster_extraction src/cluster_extraction.cpp)
target_link_libraries (cluster_extraction ${PCL_LIBRARIES})
