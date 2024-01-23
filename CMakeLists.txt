cmake_minimum_required(VERSION 3.10)  # Minimum version of CMake required

project(MySimpleProject)  # Name of your project

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Include the source files from the src directory
include(src/sources.cmake)

# Add an executable target based on the source files
add_executable(MySimpleProject ${SOURCES})

# Add the project root directory to the include path
target_include_directories(MySimpleProject PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
