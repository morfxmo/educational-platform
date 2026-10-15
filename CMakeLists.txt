cmake_minimum_required(VERSION 3.16)

project(educational-platform LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(SOURCES
    src/main.cpp
    src/System.cpp
    src/Student.cpp
    src/Doctor.cpp
)

set(HEADERS
    headers/Student.h
    headers/Doctor.h
    headers/System.h
    headers/AssignmentAnswer.h
    headers/Course.h
)

add_executable(educational-platform
    ${SOURCES}
    ${HEADERS}        
)

target_include_directories(educational-platform
    PRIVATE
        ${CMAKE_SOURCE_DIR}/headers
        ${CMAKE_SOURCE_DIR}/database
        ${CMAKE_SOURCE_DIR}/src
)
