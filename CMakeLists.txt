cmake_minimum_required(VERSION 3.22)

project(project)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_COMPILER g++)                      
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_COMPILER gcc)                      
add_definitions(-g -O2 -Wall -Wextra) 

file (GLOB SOURCES
    "./src/*.cc"
    "./src/*.c"
    )

file (GLOB HEADERS
    "./src/*.hh"
    "./src/*.h"
    )


add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(${PROJECT_NAME} PRIVATE ${HEADERS})
