
set(LEXER_SOURCES lexer.c)

add_library(LEXER_LIB STATIC ${LEXER_SOURCES})

target_link_libraries(LEXER_LIB PUBLIC TOKEN_LIB)
target_include_directories(LEXER_LIB PUBLIC ${CMAKE_SOURCE_DIR}/include)