cmake_minimum_required(VERSION 3.22)
project(Kbe VERSION 1.0)

#option(BUILD_SHARED_LIBS "Build using shared libraries" ON)
#set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}")

add_library(KbeConfigs INTERFACE)
target_compile_features(KbeConfigs INTERFACE cxx_std_17)

add_subdirectory(src)