cmake_minimum_required(VERSION 3.15)
project(server CXX)

find_package(cppzmq REQUIRED)

add_executable(${PROJECT_NAME} src/main.cpp)

target_link_libraries(${PROJECT_NAME} cppzmq)