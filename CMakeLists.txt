cmake_minimum_required(VERSION 3.13)
project(malloc VERSION 0.1 DESCRIPTION "Alexandre Waeles malloc implementation")

set(CMAKE_CXX_STANDARD 14)

# Source files
file(GLOB_RECURSE SOURCE_FILES
		${CMAKE_SOURCE_DIR}/sources/*.c
		${CMAKE_SOURCE_DIR}/sources/*.cpp)

# Header files
file(GLOB_RECURSE HEADER_FILES
		${CMAKE_SOURCE_DIR}/sources/*.h
		${CMAKE_SOURCE_DIR}/sources/*.hpp)

add_library(${PROJECT_NAME} SHARED ${HEADER_FILES} ${SOURCE_FILES})

target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_SOURCE_DIR}/include)
