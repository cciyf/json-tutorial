cmake_minimum_required (VERSION 2.6)
project (tutorial01 C)

if (CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -ansi -pedantic -Wall")
endif()

add_library(leptjson_tutorial01 leptjson.c)
add_executable(tutorial01 test.c)
target_link_libraries(tutorial01 leptjson_tutorial01)
