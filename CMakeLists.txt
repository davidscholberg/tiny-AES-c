cmake_minimum_required(VERSION 3.12)

project(tiny-aes C)

add_library(${PROJECT_NAME} "")
target_sources(${PROJECT_NAME}
    PRIVATE
        ${CMAKE_CURRENT_LIST_DIR}/aes.c
    INTERFACE
        ${CMAKE_CURRENT_LIST_DIR}/include/tiny-aes.h
        ${CMAKE_CURRENT_LIST_DIR}/include/tiny-aes.hpp
)

target_include_directories(${PROJECT_NAME}
    PUBLIC
        ${CMAKE_CURRENT_LIST_DIR}/include
)
