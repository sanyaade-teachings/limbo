add_executable (sudoku sudoku.cc)
target_link_libraries (sudoku LINK_PUBLIC limbo)


# add_test (NAME sudokus COMMAND ./test-sudokus.sh)


#find_package (Emscripten)
#if (EMCC)
#        if (CMAKE_BUILD_TYPE MATCHES Release)
#                separate_arguments(FLAGS UNIX_COMMAND "${CMAKE_CXX_FLAGS} ${CMAKE_CXX_FLAGS_RELEASE}")
#                add_custom_command (OUTPUT sudoku-js.js sudoku-js.js.mem
#                    COMMAND ${EMCC} ${FLAGS} -I../../src sudoku-js.cc -o sudoku-js.js
#                                -s EXPORTED_FUNCTIONS=['_limbo_init','_limbo_play_turn']
#                                -s TOTAL_MEMORY=67108864
#                        DEPENDS sudoku-js.cc "*.h"
#                        VERBATIM)
#
#                add_custom_target (sudoku-js DEPENDS sudoku-js.js sudoku-js.js.mem)
#                add_dependencies (sudoku sudoku-js)
#        endif ()
#endif ()


