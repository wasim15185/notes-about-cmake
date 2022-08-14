cmake_minimum_required(VERSION 3.8)

project("notes-about-library")


add_subdirectory(math) # see that i write "math" before "main" because math is library and this library liking with "main" which containing executable
add_subdirectory(main)