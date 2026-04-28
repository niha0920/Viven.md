Exception handling is a mechanism used in programming to **detect, manage, and respond to runtime errors** (exceptions) so that the program doesn’t crash abruptly and can continue or terminate gracefully.
## What is an Exception?
An **exception** is an abnormal event that occurs during the execution of a program.
### Examples:
- Division by zero
- Accessing invalid memory
- File not found
- Network failure
## Why Exception Handling?
Without exception handling:
- Program **terminates suddenly**
- Resources may not be released properly
- Poor user experience
###
With exception handling:
- Errors are handled **gracefully**
- Program flow can continue
- Debugging becomes easier
## Basic Concepts
### 1. Try Block
Contains code that might cause an exception.
### 2. Catch Block
Handles the exception if it occurs.
### 3. Finally Block
Executes **always**, whether an exception occurs or not.
### 4. Throw
Used to **generate an exception explicitly**.
## General Syntax (C++ / Java style)
```c++
try {
    // risky code
}
catch (ExceptionType e) {
    // handle exception
}
finally {
    // cleanup code (optional in C++)
}
```
## Example (C++)
```c++
#include <iostream>
using namespace std;
int main() {
    int a = 10, b = 0;
    try {
        if (b == 0)
            throw "Division by zero error!";
        cout << a / b;
    }
    catch (const char* msg) {
        cout << "Exception caught: " << msg;
    }
    return 0;
}
```
- Output:
```
Exception caught: Division by zero error!
```
## Example (Python)
```python
try:
    a = 10
    b = 0
    print(a / b)
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("Execution completed")
```
## Types of Exceptions
### 1. Built-in Exceptions
- ArithmeticException
- NullPointerException
- IndexOutOfBoundsException
### 2. User-defined Exceptions
Created by programmers for specific conditions.
## Advantages
- Prevents program crash
- Improves reliability
- Separates error-handling code from normal code
- Helps in debugging
## In Embedded / ARM Context
In systems like **ARM processors**, traditional high-level exception handling (like try-catch) is not used directly.
###
Instead, exceptions refer to:
- **Interrupts**
- **Reset**
- **Undefined instruction**
- **Software interrupt (SWI)**
###
These are handled using:
- **Exception vectors**
- **Interrupt Service Routines (ISR)**
## Summary
Exception handling:
- Deals with runtime errors
- Uses constructs like `try`, `catch`, `finally`
- Ensures smooth program execution
- In ARM → handled via hardware-level exception mechanisms
