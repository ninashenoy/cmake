cmake_minimum_required(VERSION 3.0.0)
project(add VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(app main.cpp)

target_link_libraries(app PUBLIC math)


set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
