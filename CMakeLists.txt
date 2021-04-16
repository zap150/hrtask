cmake_minimum_required(VERSION 3.5)
project(hrtask)

include(cmake/macros.cmake)

check_insource()
setup_compiler()

enable_OpenMP()

set(project_SOURCES
  main.cpp
)

add_executable(run ${project_SOURCES})
target_include_directories(run PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
