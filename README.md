
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

**First-step (Creating Library) :**

`add_library(lib_name file1.cpp file2.cpp file3.hpp ...)` <-- this line is **creating library** *(Static Library [by default])*

that's why i write to create library where `hello_lib` *library-name* `add_library( hello_lib  hello.hpp hello.cpp )` in Root `CMakeLists` 

**Second-step (Creating executable) :**

`add_executable(executable-name main1.cpp ,main2.cpp)` <-- this line is **creating executable**   

that's why i write to create executable where `simple-example` *executable-name* `add_executable(simple-example main.cpp)` in Root `CMakeLists` 

**Third-step (Linking the Library with executable) :**

`target_link_libraries(executable-name  PRIVATE/PUBLIC   lib_name)` <-- this line is *linking* **library** with **executable**

here we *linking*  `simple-example` **executable** with `hello_lib` **library** using `target_link_libraries(simple-example  PRIVATE   hello_lib)`

                    sub-dir-library-creation
                            └───build (dir) 
                            │
                            │ 
                            ├───main(dir)
                            │    └───main.cpp
                            │      └───CMakeLists.txt   
                            │    
                            │ 
                            └───math(dir)
                            │    └───src (dir)
                            │        └───add (dir)
                            │            └───add.hpp
                            │            └───add.cpp
                            │            └───CMakeLists.txt  
                            │
                            │
                            └───CMakeLists.txt 

                            ( sub-dir-library-creation  folder structure )


**First-Step (Creating `math` Library) :**
There have `CMakeLists.txt` & `src` in `math` folder . And the *add.cpp* & *add.hpp* is nested there .

Inside `CMakeLists.txt` : 

we add `add_library(math_lib  src/add/add.hpp  src/add/add.cpp)` <-- Where **`math_lib`** is `Library-Name`

then we added `target_include_directories(math_lib PUBLIC "${CMAKE_CURRENT_SOURCE_DIR/src}")` <- This helps esalier to include directory in include system `CMAKE_CURRENT_SOURCE_DIR`means the  **current CMakeList location indicrectory** (know about read the open this CMakeLists.txt)

**Second-Step (linking `math` Library with `simple-example-two`) :**