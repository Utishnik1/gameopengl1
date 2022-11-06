cmake_minimum_required(VERSION 3.2 FATAL_ERROR)

set(project_name GameFirst)
project(${project_name})

add_executable(${project_name} src/main.c)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${project_name} glfw)