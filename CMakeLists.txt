cmake_minimum_required(VERSION 3.0.0)
project(opengl_intro VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(opengl_intro src/main.cpp include/glad/glad.c)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

add_subdirectory(include/)
target_link_libraries(opengl_intro PRIVATE glad glfw)

