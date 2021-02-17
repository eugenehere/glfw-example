cmake_minimum_required(VERSION 3.19.5 FATAL_ERROR)

project(MyProject)

add_executable(MyProject src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(path/to/glfw)

target_link_libraries(myapp glfw)

find_package(OpenGL REQUIRED)

target_link_libraries(myapp OpenGL::GL)

