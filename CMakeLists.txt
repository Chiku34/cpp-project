cmake_minimum_required(VERSION 3.10.2)
project(CPPProject)

option(BUILD_TESTS "Turn on build for tests of CPPProject" OFF)

file(GLOB SRC_FILES
        "src/*.cpp"
)

set(INC_FILES_DIR
    include/
)

if(BUILD_TESTS)
    add_subdirectory(test)
endif()

include_directories(${INC_FILES_DIR})

add_executable(tictac-toe
    ${SRC_FILES}
)




