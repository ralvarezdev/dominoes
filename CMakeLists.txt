cmake_minimum_required(VERSION 3.28)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

project(Dominoes LANGUAGES CXX)

add_executable(${PROJECT_NAME} ./src/main.cpp)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/src/lib)

target_include_directories(${PROJECT_NAME}
  PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/lib)

target_link_libraries(${PROJECT_NAME}
  PRIVATE lib
)