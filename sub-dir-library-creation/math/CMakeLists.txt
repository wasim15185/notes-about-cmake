


# add_library(lib_name cppfiles...) <- this things is creating library
add_library(
    math_lib # <-- library name
    src/add/add.hpp #<- this files will according to nested CMakeLists.txt
    src/add/add.cpp
)

target_include_directories(math_lib PUBLIC "${CMAKE_CURRENT_SOURCE_DIR/src}") # kaj library include e help kora eg:  amra jodi jekono jaiga the "add.hpp" or "add.cpp" include korte chai tahole sekhane include"src/add/add.hpp" likhi tahole library import hoye gelo
      #                                   "this CMakeLists.txt current location"/src                                  