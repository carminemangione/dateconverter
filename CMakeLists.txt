cmake_minimum_required(VERSION 3.14)
project(testing_test)

set(CMAKE_CXX_STANDARD 14)

set(SOURCE_FILES main.cpp Google_tests/AbsoluteDateTest.cpp Google_tests/ConverterTests.cpp)
add_executable(DateConverter_run ${SOURCE_FILES})

include_directories(DateConverter_lib)
add_subdirectory(DateConverter_lib)
add_subdirectory(Google_tests)

target_link_libraries(DateConverter_run DateConverter_lib)

