add_executable(Main main.cpp)  # <-- 'simple-example-two' is executable-name

target_link_libraries(Main  PRIVATE   math_lib) 