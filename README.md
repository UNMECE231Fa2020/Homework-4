# Homework4

## Instructions
In a previous lecture, I created a generic single linked list class. For this assignment, you will convert my linked list class into a generic doubly linked list class. Fortunately, I've done about 1/3 of the work for you. I updated some the single linked list to become a doubly linked list. I updated the private data as well as these methods:

    Constructors
    Destructors
    Getters
    
Your job now is to update the following methods:

    add_front
    add_back
    rm_front
    rm_back
    empty()
    print()
    
You are also going to overload the `=` operator to copy one generic list to another generic list.

    List &operator=(const List &x)
    
Using `x` as the input variable, you must create a loop that iterates from `x._front` until the `nullptr`, calling `push_back` in the body of you code. Remember, `x._front` is a doubly linked list that should be moving forward, keep that in mind as you step through the loop. Also, I recommend using `auto` as the datatype for your iterator.

You'll be provided with a file `main.cpp` that will test your class, as well as `GeneralList.hpp`. You will need to finishing implementing the `List` class in `GeneralList.hpp`. Feel free to rename `GeneralList.hpp` to somthing else using the `git mv` command.

## Rubric
    Executable runs with no errors: 20%
    Implementation of methods in GeneralList.hpp: 40%
    Creation of Makefile: 20%
    Clean code: 20%
