# Role of Functions
In C programming, **functions** are one of the most important building blocks. They help organize code, improve readability, and make programs easier to maintain and reuse.
## What is a Function?
A **function** is a block of code that performs a specific task and can be called (invoked) whenever needed.
```c
return_type function_name(parameters) {
    // body of the function
}
```
## Role of Functions in C
### 1. Code Reusability
Instead of writing the same code multiple times, you can write it once inside a function and reuse it.
```c
int add(int a, int b) {
    return a + b;
}
```
## 2. Modularity (Divide and Conquer)
Large programs can be divided into smaller parts (functions), making them easier to understand and manage.
### Example:
- One function for input
- One for processing
- One for output
## 3. Improves Readability
Functions make code more structured and easier to read.
### Instead of:
```c
// long complex code
```
You can write:
```c
calculateSalary();
displayReport();
```
## 4. Ease of Debugging
If an error occurs, you only need to check the specific function instead of the entire program.
## 5. Abstraction
Functions hide implementation details. You just call the function without worrying about how it works internally.
```c
printf("Hello");
```
You don’t need to know how `printf` works internally.
## 6. Reduces Code Size
Using functions avoids repetition, which reduces the overall code length.
## 7. Facilitates Team Work
Different developers can work on different functions simultaneously.
## Types of Functions in C
### 1. Library Functions
Predefined functions provided by C.
#### Examples:
- `printf()`
- `scanf()`
- `strlen()`
## 2. User-defined Functions
Functions created by the programmer.
## Example Program
```c
#include <stdio.h>
int square(int num) {
    return num * num;
}
int main() {
    int result = square(5);
    printf("Square = %d", result);
    return 0;
}
```
## Summary
Functions in C:
- Promote **reusability**
- Provide **modularity**
- Improve **readability**
- Simplify **debugging**
- Enable **abstraction**

# Passing arguments to functions
Passing arguments to functions in C is about **how data is sent from the calling function (usually `main`) to the called function**.
## What are Arguments?
- **Arguments** are the actual values passed to a function when it is called.
- **Parameters** are the variables in the function definition that receive those values.
```c
int add(int a, int b)  // parameters
{
    return a + b;
}
add(5, 3);  // arguments
```
## Ways of Passing Arguments in C
### 1. Call by Value (Default in C)
- A **cop**y of the actual argument is passed.
- Changes inside the function **do NOT affect** the original variable.
```c
#include <stdio.h>
void modify(int x) {
    x = x + 10;
    printf("Inside function: %d\n", x);
}
int main() {
    int a = 5;
    modify(a);
    printf("Outside function: %d", a);
    return 0;
}
```
#### Output:
```
Inside function: 15
Outside function: 5
```
Original value is unchanged.
## 2. Call by Reference (Using Pointers)
- Address of the variable is passed.
- Changes inside the function **affect the original variable**.
```c
#include <stdio.h>
void modify(int *x) {
    *x = *x + 10;
}
int main() {
    int a = 5;
    modify(&a);
    printf("Value: %d", a);
    return 0;
}
```
### Output:
```c
Value: 15
```
Original value is modified.
## Key Differences
| Feature            | Call by Value       | Call by Reference |
| ------------------ | ------------------- | ----------------- |
| What is passed     | Copy of value       | Address (pointer) |
| Effect on original | No change           | Changes occur     |
| Memory usage       | More (copy created) | Efficient         |
| Safety             | Safer               | Risky if misused  |
## Why Use Each?
- **Call by Value**
  - When you don’t want to modify original data
  - Safer and simpler
- **Call by Reference**
  - When you need to modify original variables
Efficient for large data (arrays, structures)
## Example: Swap Using Call by Reference
```c
#include <stdio.h>
void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}
int main() {
    int x = 10, y = 20;
    swap(&x, &y);
    printf("x=%d y=%d", x, y);
    return 0;
}
```
## Summary
- **Arguments → values passed**
- **Parameters → variables receiving them**
- Two ways:
  - **Call by Value** (safe, no change)
  - **Call by Reference** (modifies original)
 
# Returning values from functions
