cmake_minimum_required (VERSION 3.3)
project (Engine)

set(DEP_PATH "$ENV{ENGINE_DEPENDENCIES_PATH}")

message("Looking for ENGINE_DEPENDENCIES_PATH: " $ENV{ENGINE_DEPENDENCIES_PATH})
if(DEP_PATH)
    add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/Input)
    add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/Shader)
else()
    message([FATAL_ERROR] "CMake Error, ENGINE_DEPENDENCIES_PATH environment variable has not been found, you must declare it if you want install Libraries")
endif()