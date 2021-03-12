cmake_minimum_required(VERSION 3.10)

project(prototype.out)

find_package(SDL2 REQUIRED)
include_directories(SDL2::SDL2 SDL2::SDL2main)

find_package(OpenGL REQUIRED COMPONENTS OpenGL)
include_directories(OpenGL::OpenGL)

find_package(GLEW REQUIRED)
include_directories(GLEW::GLEW)

add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME} SDL2::SDL2 SDL2::SDL2main)
target_link_libraries(${PROJECT_NAME} OpenGL::OpenGL GLEW::GLEW)
