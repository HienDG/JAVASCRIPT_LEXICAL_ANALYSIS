cmake_minimum_required(VERSION 3.10.0)
project(JAVASCRIPT_LEXICAL_ANALYSIS VERSION 0.1.0 LANGUAGES C)

set(CMAKE_C_STANDARD 17)
set(CMAKE_C_STANDARD_REQUIRED ON)

set(MAIN_SOURCES src/main.c)
add_subdirectory(src/token)
add_subdirectory(src/lexer)

add_executable(${PROJECT_NAME} ${MAIN_SOURCES})

target_link_libraries(${PROJECT_NAME} PRIVATE TOKEN_LIB LEXER_LIB)
target_link_directories(${PROJECT_NAME} PRIVATE include)
