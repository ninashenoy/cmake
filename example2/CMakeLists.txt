cmake_minimum_required(VERSION 3.0.0)
project(add VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(math
    src/add.cpp
    src/sub.cpp
    src/main.cpp)

#we are adding an include directory for target math and the directory's name is 'inc'
#it is located in the folder where CMakeLists.txt is found
target_include_directories(math PUBLIC inc)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
