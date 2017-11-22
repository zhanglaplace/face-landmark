cmake_minimum_required(VERSION 2.9)
project(facelandmark)

#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV)
find_package(Caffe REQUIRED)
#message(FATAL_ERROR ${Caffe_INCLUDE_DIRS})
include_directories(${Caffe_INCLUDE_DIRS})

link_directories(/home/zf/Downloads/dlib-19.7/build/dlib/) #dlib编译后bulid下dlib地址
set(SOURCE_FILES face_landmark.cpp)
add_executable(facelandmark ${SOURCE_FILES})
target_link_libraries(facelandmark dlib ${OpenCV_LIBS} )
target_link_libraries(facelandmark ${Caffe_LIBRARIES})
