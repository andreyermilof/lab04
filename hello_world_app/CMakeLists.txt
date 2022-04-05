cmake_minimum_required(VERSION 3.0)

project(hello)

add_executable(${PROJECT_NAME} hello_world.cpp)

set_target_properties(${PROJECT_NAME} PROPERTIES
                        CMAKE_CXX_STANDARD 17
                        CMAKE_CXX_STANDARD_REQUIRED ON
                        CMAKE_BUILD_TYPE Release)

target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex formatter_ex)

target_link_libraries(${PROJECT_NAME} formatter_ex)