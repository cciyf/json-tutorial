cmake_minimum_required (VERSION 2.6)
project (tutorial02_answer C)

if (CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -ansi -pedantic -Wall")
endif()

add_library(leptjson leptjson.c)
add_executable(tutorial02_answer test.c)
target_link_libraries(tutorial02_answer leptjson)
