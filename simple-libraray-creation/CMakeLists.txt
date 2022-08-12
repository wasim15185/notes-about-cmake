cmake_minimum_required(VERSION 3.8)

project("notes-about-library")

# add_library(lib_name cppfiles...) <- this things is creating library
add_library(
    hello_lib # <-- library name
    hello.hpp
    hello.cpp
)

add_executable(simple-example main.cpp)  # <-- 'simple-example' is executable-name

target_link_libraries(simple-example  PRIVATE   hello_lib)  # With help of this method we linking the library ( hello_lib ) with executable (simple_example) 

#                   executable-name             library name
