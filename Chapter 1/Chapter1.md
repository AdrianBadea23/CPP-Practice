# Basics of a C++ program

- statement - type of instruction that tells a program what to do - smallest independent unit of the C++ language.
- one statement => many machine language instructions
- statements are grouped into units called functions => function = collection of statements

```C++
    #include <iostream>

    int main()
    {
    std::cout << "Hello world!";
    return 0;
    }
```

- first line = preprocessor directive that indicates that we would like to use the contents of the iostream library.

- main function - every program must have a main function or it will fail to link
- {} - tell the program what is considered part of the main function
- `std::cout` - character output aka will print information in the console
- return - returns 0 to the operating system to signal that everything worked correctly 

## Data and values

- data = any informtaion that can be moved, processed or stored by a computer
- a single piece of data is called a value

## Random access memory

- when we run a program the OS loads the memory into RAM, any data that is hardcoded at this point is loaded at this point

- the os also reserves aditional data for the program to use while running

## Objects and variables

- in C++ direct memory access is discouraged
- we access data throug an object - an object being a region of storage that can store a value and has other associated properties
- an object with a name is called a variable
- int x - define a variable of name x and of type int
- when the program is run(called runtime)

## Variable intialization

```C++

int width { 5 }; // define variable width and initialize with initial value 5

// variable width now has value 5

int a;         // no initializer (default initialization)
int b = 5;     // initial value after equals sign (copy initialization)
int c( 6 );    // initial value in parenthesis (direct initialization)

// List initialization methods (C++11) (preferred)
int d { 7 };   // initial value in braces (direct list initialization)
int e = { 8 }; // initial value in braces after equals sign (copy list initialization)
int f {};      // initializer is empty braces (value initialization)

```

- when the value is provided after an equals sign it is called copy initialization.
- copy intialization has fallen out of favor in modern C++ due to it being less efficient than other forms of intialization for some complex types
- direct initialization is provided inside parenthesis - niche use
- modern C++ standard is to use list initialization(int list_init {6})

## 1.8