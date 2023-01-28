cmake_minimum_required(VERSION 3.10 FATAL_ERROR)

set(proj_name BattleCity)

project(${proj_name})

add_executable(${proj_name} src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${proj_name} glfw)
