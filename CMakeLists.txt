cmake_minimum_required (VERSION 3.0)
project(TVasAI)

set(CMAKE_BUILD_TYPE Release)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH})
#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14")

include_directories(${PROJECT_SOURCE_DIR}/include)
include_directories(${PROJECT_SOURCE_DIR}/source)

file(GLOB H_FILES ${PROJECT_SOURCE_DIR}/include/*.hpp)
file(GLOB CPP_FILES ${PROJECT_SOURCE_DIR}/source/*.cpp)

add_executable(TVasAI main.cpp  ${H_FILES} ${CPP_FILES})
#install(TARGETS TVasAI DESTINATION /usr/bin)