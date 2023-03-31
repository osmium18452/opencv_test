cmake_minimum_required(VERSION 3.23)
project(opencv_test)

set(CMAKE_CXX_STANDARD 14)
include_directories($ENV{OPENCV_INCLUDE_DIR})
#include_directories(${OpenCV_INCLUDE_DIRS})
set(OpenCV_DIR $ENV{OPENCV_BUILD})
find_package(OpenCV REQUIRED)

add_executable(opencv_test main.cpp)
target_link_libraries(opencv_test ${OpenCV_LIBS})
