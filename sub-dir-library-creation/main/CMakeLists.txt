add_executable(simple-example-two main.cpp)  # <-- 'simple-example-two' is executable-name

target_link_libraries(simple-example-two  PRIVATE   math_lib) 