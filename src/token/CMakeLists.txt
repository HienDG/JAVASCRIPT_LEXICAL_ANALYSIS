set(TOKEN_SOURCES token.c)

add_library(TOKEN_LIB STATIC ${TOKEN_SOURCES})

target_include_directories(TOKEN_LIB PUBLIC ${CMAKE_SOURCE_DIR}/include)