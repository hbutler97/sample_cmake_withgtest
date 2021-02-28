cmake_minimum_required(VERSION 3.15)
set(CMAKE_BUILD_TYPE Debug)
set(PROJECT_NAME myasiolib)
project(${PROJECT_NAME})

set(CMAKE_CXX_STANDARD 14)

find_package(BOOST 1.61 REQUIRED system thread regex)
include_directories(${Boost_INCLUDE_DIRS})
if(Boost_FOUND)
endif()
set(HEADERS
        mylib.h)

set(SOURCE
        mylib.cpp)

add_library(${PROJECT_NAME} ${HEADERS} ${SOURCE})

target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_BINARY_DIR}/lib)
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
#target_link_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
#target_link_libraries(${PROJECT_NAME} LINK_PUBLIC ${PROJECT_NAME}lib ${Boost_LIBRARIES})