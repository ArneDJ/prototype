cmake_minimum_required(VERSION 3.10)

project(prototype.out)

find_package(SDL2 REQUIRED)
include_directories(SDL2::SDL2)

add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME} SDL2::SDL2)
