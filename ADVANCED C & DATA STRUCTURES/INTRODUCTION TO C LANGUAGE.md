# Features of C
C is a powerful and widely used programming language, especially in system-level and embedded development. Here are the **key features of C** explained clearly:
## 1. Simple and Efficient
- C has a small set of keywords and straightforward syntax.
- Programs written in C are fast and efficient because it is close to hardware.
## 2. Procedural Language
- Follows a **top-down approach**.
- Programs are divided into functions (modular programming).
- Example: `main()`, user-defined functions.
## 3. Low-Level Access (Close to Hardware)
- Supports direct memory access using pointers.
- Can interact with hardware (used in OS, drivers, embedded systems).
## 4. Portability
- C programs can run on different systems with little or no modification.
- Same code can compile on Windows, Linux, etc.
## 5. Rich Set of Data Types
- Basic types: `int`, `char`, `float`, `double`
- Derived types: arrays, pointers, structures, unions
## 6. Pointers
- One of the most powerful features.
- Allows dynamic memory management and efficient data handling.
- Used in arrays, strings, and structures.
## 7. Dynamic Memory Allocation
- Memory can be allocated at runtime using:
  - `malloc()`
  - `calloc()`
  - `realloc()`
  - `free()`
## 8. Structured Programming
- Code can be organized using functions, loops, and conditionals.
- Improves readability and debugging.
## 9. Extensive Standard Library
- Provides built-in functions for:
  - Input/Output (`printf`, `scanf`)
  - String handling
  - Math operations
## 10. Preprocessor Support
- Handles directives before compilation:
  - `#include`
  - `#define`
  - `#ifdef`
## 11. Recursion
- Functions can call themselves.
- Useful for problems like factorial, tree traversal, etc.
## 12. Bitwise Operations
- Supports operations like AND, OR, XOR, shifts.
- Important in embedded and system programming.
## 13. Case Sensitive
- `main` and `Main` are different.
- Helps avoid ambiguity but requires careful coding.
## 14. Middle-Level Language
- Combines features of:
  - High-level (easy syntax)
  - Low-level (memory access)

# History
## History of C Programming Language
## Origin of C
Dennis Ritchie developed C in the early 1970s at Bell Laboratories (AT&T).
- C was created to develop the **Unix operating system**
- It was designed to overcome limitations of earlier languages like B
## Evolution Before C
### 1. BCPL (Basic Combined Programming Language) – 1960s
- Developed by Martin Richards
- Used for system programming
- Simple but lacked data types
### 2. B Language – 1970
- Developed by Ken Thompson
- Derived from BCPL
- Still limited (no data types, less powerful)
## Birth of C (1972)
- Dennis Ritchie improved B and created C
- Added:
  - Data types (`int`, `char`, etc.)
  - Better memory handling
  - More powerful operators
## C and Unix
- C became popular because it was used to rewrite the
Unix OS.
### This made Unix:
- Portable across different machines
- Easier to maintain
## Standardization of C
### 1. K&R C (1978)
- Book: The C Programming Language by Dennis Ritchie and Brian Kernighan
- First widely accepted version
### 2. ANSI C (C89 / C90)
- Standardized by American National Standards Institute
- Made C portable and consistent
### 3. Later Standards
- C99 → Added new features (inline, new data types)
- C11 → Multi-threading support
- C18 → Minor improvements and bug fixes
## Why C Became So Popular
- Fast and efficient
- Portable
- Used in OS, compilers, embedded systems
- Foundation for languages like:
  - C++
  - Java
  - Python (internally)

# Structure of C Program
## Structure of a C Program
A C program is organized into several sections. Understanding this structure is important for writing clear and maintainable code.
## Basic Structure
```c
#include <stdio.h>     // 1. Documentation / Link Section
#define PI 3.14        // 2. Definition Section
int globalVar = 10;    // 3. Global Declaration Section
int add(int a, int b); // 4. Function Declaration Section
int main()             // 5. Main Function Section
{
    int x = 5, y = 3;  // Local Declaration
    int result;
    result = add(x, y); // Function call
    printf("Sum = %d", result);
    return 0;
}
// 6. User-defined Function Section
int add(int a, int b)
{
    return a + b;
}
```
## Explanation of Each Section
## 1. Documentation Section
- Contains comments explaining the program
- Example:
```c
// Program to add two numbers
```
## 2. Link Section
- Includes header files using `#include`
- Gives access to library functions
- Example:
```c
#include <stdio.h>
```
## 3. Definition Section
- Defines constants using `#define`
- Example:
```c
#define MAX 100
```
## 4. Global Declaration Section
- Declares global variables and function prototypes
- Accessible throughout the program
## 5. Main Function Section
- Entry point of every C program
- Execution starts from `main()`
### Contains:
- Local variable declarations
- Executable statements
- Function calls
## 6. User-defined Function Section
- Functions written by the programmer
- Perform specific tasks
- Can be called from `main()`
## Execution Flow
1. Preprocessor runs (`#include`, `#define`)
2. Compilation
3. Execution starts from `main()`
4. Calls other functions as needed

# Keywords, Identifiers, Variables and Constants
## 1. Keywords in C
- **Keywords** are reserved words with predefined meanings.
- You **cannot use them as names** for variables or functions.
### Examples:
```c
int, float, char, if, else, return, while, for, void
```
### Key Points:
- Fixed meaning (defined by compiler)
- Cannot be redefined
- Typically lowercase
#### Example:
```c
int a = 10;  // 'int' is a keyword
```
## 2. Identifiers
- **Identifiers** are names given to:
  - Variables
  - Functions
  - Arrays
  - Structures
### Examples:
```c
sum, total_marks, calculateArea, _count
```
### Rules for Identifiers:
- Must start with a letter (A–Z, a–z) or `_`
- Cannot start with a number
- No spaces or special characters (`@, #, %`)
- Cannot be a keyword
- Case-sensitive (`sum` ≠ `Sum`)
#### Example:
```c
int total = 100;
```
## 3. Variables
- A **variable** is a named memory location used to store data.
- Value can **change during execution**.
### Syntax:
```c
data_type variable_name;
```
### Examples:
```c
int age = 21;
float price = 99.5;
char grade = 'A';
```
### Key Points:
- Must be declared before use
- Stored in memory
- Type defines size and operations
## 4. Constants
- **Constants** are fixed values that **do not change** during program execution.
## Types of Constants
### 1. Numeric Constants
```c
10, -25, 3.14
```
### Character Constants
```c
'A', 'b', '9'
```
### String Constants
```c
"Hello", "C Programming"
```
## Constant Declaration Methods
### (a) Using `const`
```c
const int x = 10;
```
### (b) Using `#define`
```c
#define PI 3.14
```
## Key Points:
- Value cannot be modified
- Improves readability
- Prevents accidental changes
## Quick Comparison
| **Feature**    | **Keywords**       | **Identifiers** | **Variables**         | **Constants**     |
| -------------- | ------------------ | --------------- | --------------------- | ----------------- |
| Meaning        | Reserved words     | Names           | Storage locations     | Fixed values      |
| Changeable     | No                 | —               | Yes                   | No                |
| Defined by     | Compiler           | Programmer      | Programmer            | Programmer        |
| Example        | `int`, `if`        | `sum`, `x`      | `int x = 5`           | `const x = 5`     |
