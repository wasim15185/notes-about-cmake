


# add_library(lib_name cppfiles...) <- this things is creating library
add_library(
    math_lib # <-- library name
    src/add/add.hpp #<- this files will according to nested CMakeLists.txt
    src/add/add.cpp
)

target_include_directories(math_lib PUBLIC "${CMAKE_CURRENT_SOURCE_DIR/src}")