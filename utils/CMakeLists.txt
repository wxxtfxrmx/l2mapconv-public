cmake_minimum_required(VERSION 3.17)
project(utils)

add_library(${PROJECT_NAME}
    src/Log.cpp
    src/Bitset.cpp
)

target_include_directories(${PROJECT_NAME} PUBLIC include)

# Compiler options
set_target_properties(${PROJECT_NAME} PROPERTIES
    CXX_STANDARD 20
    CXX_STANDARD_REQUIRED ON
)

target_compile_options(${PROJECT_NAME} PRIVATE -Wall -Wextra -pedantic)
