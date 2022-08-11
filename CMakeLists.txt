cmake_minimum_required(VERSION 3.22)
project(lisp C)

set(CMAKE_C_STANDARD 11)


link_libraries(edit)

include_directories(ext)
set(BUILD_DIR learning-lisp)
set(LIBRARY_OUTPUT_PATH "${BUILD_DIR}/test")
set(EXECUTABLE_OUTPUT_PATH  "${BUILD_DIR}")

set(MPC_FILES
        ext/mpc.c
#        test/doge_code.c
#        test/doge_grammar.c
#        main/prompt.c
#        main/parsing.c
        main.c)

add_executable(lisp ${MPC_FILES})
