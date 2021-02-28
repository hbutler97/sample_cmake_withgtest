cmake_minimum_required(VERSION 3.15)
set(PROJECT_NAME app1)

find_package(GTest REQUIRED)
include_directories(${GTEST_INCLUDE_DIRS})

set(SOURCE main.cpp)

add_executable(${PROJECT_NAME} ${SOURCE})
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_BINARY_DIR}../lib)

target_link_libraries(${PROJECT_NAME} PUBLIC ${GTEST_LIBRARIES} myasiolib pthread)

