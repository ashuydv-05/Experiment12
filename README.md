# Experiment12
## AIM:-
Constructors in C++
## Software used:-
VS code
## Theory:-
A constructor in C++ is a special member function that is used to initialize the variables of a class when an object is created.
### Key Features
1. Name Matching: The constructor's name matches exactly with the class name.
2. No Return Type: Constructors do not have a return type, not even void.
3. Automatic Invocation: A constructor is automatically invoked when an object of the class is instantiated.
4. Initialization: Primarily used to initialize member variables of the class.
### Access Control
1. Public Section: Constructors are typically declared in the public section of a class to allow easy creation of objects.
2. Private or Protected Sections: Can also be declared in the private or protected sections to restrict object creation.
### Constructor Overloading
Multiple Constructors: Constructors can be overloaded, allowing multiple ways of initializing an object.
Restrictions: Constructors cannot be declared as virtual functions.
### Syntax
Inside Class Definition:
```
ClassName(parameters) { 
    // implementation 
}
```

