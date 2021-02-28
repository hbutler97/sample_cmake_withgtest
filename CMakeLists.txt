cmake_minimum_required(VERSION 3.15)
project(asio_experiment)

add_subdirectory(lib)
add_subdirectory(gtest)
add_subdirectory(app1)
set(CMAKE_CXX_STANDARD 14)

add_executable(asio_experiment main.cpp)