CMAKE_MINIMUM_REQUIRED(VERSION "2.8.11")

PROJECT("tiny-regex-c" C)

INCLUDE_DIRECTORIES(".")

ADD_LIBRARY("tiny-regex-c" STATIC
        re.c
        )

ADD_TEST(NAME make_test
        WORKING_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}"
        COMMAND make test
        )
