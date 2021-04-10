cmake_minimum_required (VERSION 3.17)
project (SoberExample)

set (CMAKE_CXX_STANDARD 17)
include ("${CMAKE_SOURCE_DIR}/CMake/Sober/Sober.cmake")
enable_testing ()

# WARNING: All targets, that use services, must be defined after used services.
add_subdirectory (Service)
add_subdirectory (Library)
add_subdirectory (Test)
add_subdirectory (Executable)