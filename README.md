
## Example 1 . simple-libraray-creation 
#### (Here we create simple library)


Here we simple library called **`hello_lib`** and link with  **`simple-example`** executable 

            simple-libraray-creation
                └───build (folder) 
                │ 
                │     
                ├───hello.cpp
                ├───hello.hpp
                └───main.cpp
                (  simple-libraray-creation  folder structure )


### Now we will how to create simple library !


**Note** there no sub dircectory there are **no extra CMakeLists** there are **Only one CMakeLists** 

**First-step  :**

`add_library(lib_name file1.cpp file2.cpp file3.hpp ...)` <- this line is creating library

that's why i write to create library `add_library( hello_lib  hello.hpp hello.cpp )` in Root `CMakeLists`
                                                    |           |           |
                                                                 ------------
                                              **Lib-Name**         **Cpp Files**       




