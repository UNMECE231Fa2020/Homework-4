# Homework3
Fourth homework of ECE 231: Intermediate Programming. Assigned 2/14/2020. Due 2/21/2020, 11:59 pm.

## Instructions
A class will be created that will act like a container for a doubly linked list. However, the class will not be held down by an particular data type. This will be done with templates. The class will be called `List` and the template declaration for the class will look like this:

    template<class T> class List
    
The letter `T` can change, and can be change to whatever you want. Below is an example of the private data members should look like:
    
    template<class T> class List {
      private:
      struct _list {
        T value;
        struct _list *next;
        struct _list *prev;
      };
      typedef struct _list Dlist;
      
      size_t _size;
      Dlist *_front;
      Dlist *_back;
      
      void reccopy(const Dlist *ptr) {
        if(ptr) {
          reccopy(ptr->next);
          //push_front(ptr->value);
        }
      }
      
Uncomment the line `push_front(ptr->value)` after you have implemented the function `push_front`. Additionally, you can change `T`, `_list`, `Dlist`, and `ptr` to whatever you want, just make sure to stay consistent. You are going to implement two constructors, a default constructor, and a copy constructor. The copy constructor should call `reccopy`.

    List()
    List(const List &x)
    
Where `x` is a variable of your choosing. You must also implement a destructor that removes all nodes using `pop_front`.

    ~List()
    
Three getters need to be implemented, one what gets the first value of the list, the last value of the list, and the size of the list.

    front()
    back()
    size()
    
You are also going to overload the `=` operator to copy the class to another class

    List &operator=(const List &x)
Where `x` is a variable of your choosing.
