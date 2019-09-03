cmake_minimum_required(VERSION 3.14..3.15 FATAL_ERROR)

include(FetchContent)

# ------------------------------------------------------------------------------
# The fastest feature-rich C++11/14/17/20 single-header testing framework for
# unit tests and TDD
FetchContent_Declare(
        extern_doctest
        GIT_REPOSITORY https://github.com/onqtam/doctest.git
        GIT_TAG        2.3.4)

FetchContent_GetProperties(extern_doctest)
if(NOT extern_doctest_POPULATED)
    FetchContent_Populate(extern_doctest)
    add_subdirectory(
            ${extern_doctest_SOURCE_DIR}
            ${extern_doctest_BINARY_DIR}
            EXCLUDE_FROM_ALL)
endif()

# ------------------------------------------------------------------------------
# A multi-platform library for OpenGL, OpenGL ES, Vulkan, window and
# input http://www.glfw.org/
FetchContent_Declare(
        extern_glfw
        GIT_REPOSITORY https://github.com/glfw/glfw.git)

FetchContent_GetProperties(extern_glfw)
if(NOT extern_glfw_POPULATED)
    FetchContent_Populate(extern_glfw)
    add_subdirectory(
            ${extern_glfw_SOURCE_DIR}
            ${extern_glfw_BINARY_DIR}
            EXCLUDE_FROM_ALL)
endif()

# ------------------------------------------------------------------------------
# Cross-platform asynchronous I/O
# http://libuv.org
FetchContent_Declare(
        extern_libuv
        GIT_REPOSITORY https://github.com/libuv/libuv.git
        GIT_TAG v1.31.0)

FetchContent_GetProperties(extern_libuv)
if(NOT extern_libuv_POPULATED)
    FetchContent_Populate(extern_libuv)
    add_subdirectory(
            ${extern_libuv_SOURCE_DIR}
            ${extern_libuv_BINARY_DIR}
            EXCLUDE_FROM_ALL)
endif()

