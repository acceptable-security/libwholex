# libwholex

## Overview
libwholex is a very simple lexical analysis library for C programs.

## Usage
Unfortunately there is no definite documentation for the API, however this is a brief overview of the API.

    lexer_state_t* lexer_init(const char* src, const char* specialTokens[]);
    void lexer_error(lexer_state_t* lex, const char* error, ...);
    void lexer_debug(lexer_state_t* lex);
    void lexer_clean(lexer_state_t* lex);

    token_t* lexer_cur(lexer_state_t* lex);
    token_t* lexer_lookahead(lexer_state_t* lex);
    bool lexer_matches(lexer_state_t* lex, token_types_t tokentype);
    bool lexer_lookaheadmatches(lexer_state_t* lex, token_types_t tokentype);
    token_t* lexer_next(lexer_state_t* lex);
    token_t* lexer_nextif(lexer_state_t* lex, token_types_t tokentype);
    token_t* lexer_nextif_special(lexer_state_t* lex, const char* token);
    token_t* lexer_expect(lexer_state_t* lex, token_types_t tokentype);
    token_t* lexer_expect_special(lexer_state_t* lex, const char* token);
    token_t* lexer_expectmatch(lexer_state_t* lex, const char* end, const char* start, int linenum);

## Building
    mkdir build
    bfg9000 . build/
    cd build
    make

## Installing
Not quite sure how to do this yet with bfg9000, so anyone who could tell me would be really cool.

## Tests
TODO :)
