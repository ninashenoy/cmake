cmake_minimum_required(VERSION 3.0.0)
project(math VERSION 0.1.0)

include(CTest)
enable_testing()

add_library(math
    src/add.cpp
    src/sub.cpp)

target_include_directories(math PUBLIC inc)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
