cmake_minimum_required(VERSION 3.14 FATAL_ERROR)


#
# Configure CMake environment
#


# Include cmake modules
list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake")


# Define Project
set(RUSHMORE_VERSION 0.0.1.0)
project(rushmore)

# Add project modules
add_subdirectory(external)
#add_subdirectory(core)
