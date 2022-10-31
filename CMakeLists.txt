cmake_minimum_required(VERSION 3.16)

project(BurtOS-2 DESCRIPTION "Base station and rover computer software for Binghamton University Rover Team (BURT)")

# Output binary files in more accessible locations than in the source subdirectories
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)

add_subdirectory(src/events)
add_subdirectory(src/network)
add_subdirectory(src/rover_control)
add_subdirectory(src/subsystem)
