cmake_minimum_required(VERSION 3.0)

project(formatter)

add_library(${PROJECT_NAME} STATIC formatter.cpp)

set_target_properties(${PROJECT_NAME} PROPERTIES
                        CMAKE_CXX_STANDARD 17
                        CMAKE_CXX_STANDARD_REQUIRED ON
                        CMAKE_BUILD_TYPE Release)