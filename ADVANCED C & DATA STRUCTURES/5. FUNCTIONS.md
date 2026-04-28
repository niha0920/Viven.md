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
Returning values from functions in C is how a function **sends results back to the calling function**.
## What is a Return Value?
A **return value** is the result that a function gives back using the `return` statement.
```c
return expression;
```
## Basic Example
```c
#include <stdio.h>
int add(int a, int b) {
    return a + b;   // returning value
}
int main() {
    int result = add(3, 4);  // receiving value
    printf("Sum = %d", result);
    return 0;
}
```
## How It Works
1. Function is called → `add(3, 4)`
2. Control goes to function
3. Calculation happens
4. `return` sends value back
5. Control returns to caller
## Types of Return in Functions
### 1. Function Returning a Value
```c
int square(int x) {
    return x * x;
}
```
- Must have a return type (`int`, `float`, etc.)
## 2. Function Returning Nothing (`void`)
```c
void display() {
    printf("Hello");
}
```
- No value is returned
- `return;` is optional
## 3. Returning Multiple Values (Using Pointers)
C functions return only one value directly, but multiple values can be returned using pointers.
```c
#include <stdio.h>
void calculate(int a, int b, int *sum, int *product) {
    *sum = a + b;
    *product = a * b;
}
int main() {
    int s, p;
    calculate(3, 4, &s, &p);
    printf("Sum=%d Product=%d", s, p);
    return 0;
}
```
## Important Rules
### 1. Return Type Must Match
```c
int func() {
    return 5;   // correct
}
```
```c
int func() {
    return 5.5; // type mismatch (implicit conversion)
}
```
## 2. Only One Value is Returned
- Even if multiple `return` statements exist, only one executes.
```c
int check(int x) {
    if (x > 0)
        return 1;
    else
        return -1;
}
```
## 3. `return` Ends Function Execution
Any code after `return` is not executed.
## 4. Functions Can Return Expressions
```c
return a + b * c;
```
## Special Cases
### Returning Arrays
- Not directly possible
- Use pointers or structures
### Returning Pointers
```c
int* getPointer(int *p) {
    return p;
}
```
## Summary
- `return` sends data back to caller
- Return type must match function declaration
- Only one value returned directly
- Multiple values → use pointers

# Recursive Functions
## Recursive Functions in C
A **recursive function** is a function that **calls itself** to solve a problem. It breaks a big problem into smaller subproblems of the same type.
## Basic Idea
Every recursive function must have:
1. **Base Case** → Condition to stop recursion
2. **Recursive Case** → Function calls itself with smaller input
## Syntax
```c
return_type function_name(parameters) {
    if (base_condition)
        return value;
    return function_name(smaller_input); // recursive call
}
```
## Example 1: Factorial
Factorial formula:
- n! = n × (n-1)!
- 0! = 1 (base case)
```c
#include <stdio.h>
int factorial(int n) {
    if (n == 0)
        return 1;   // base case
    else
        return n * factorial(n - 1);  // recursive call
}
int main() {
    printf("%d", factorial(5));
    return 0;
}
```
### Flow:
```
factorial(5)
→ 5 * factorial(4)
→ 5 * 4 * factorial(3)
→ ...
→ 5 * 4 * 3 * 2 * 1
```
## Example 2: Fibonacci Series
```c
#include <stdio.h>
int fib(int n) {
    if (n <= 1)
        return n;   // base case
    return fib(n-1) + fib(n-2);
}
int main() {
    printf("%d", fib(6));
    return 0;
}
```
## How Recursion Works (Stack Concept)
- Each function call is stored in **call stack**
- When base case is reached → stack starts **unwinding**
- Values are returned step by step
## Advantages
- Code is **short and clean**
- Useful for problems like:
  - Factorial
  - Fibonacci
  - Tree traversal
  - Divide & conquer (merge sort, quicksort)
## Disadvantages
- Uses more memory (stack)
- Slower than iteration (function call overhead)
- Risk of **stack overflow** if base case is missing
## Recursion vs Iteration
| Feature  | Recursion             | Iteration         |
| -------- | --------------------- | ----------------- |
| Approach | Function calls itself | Loops (for/while) |
| Memory   | Uses stack            | Less memory       |
| Speed    | Slower                | Faster            |
| Code     | Cleaner               | Longer sometimes  |
## Example: Infinite Recursion (Wrong)
```c
void fun() {
    fun();  // no base case
}
```
- This leads to **stack overflow**
## Summary
- Recursive function = function calling itself
- Must have **base case + recursive case**
- Uses **call stack**
- Good for complex problems but can be memory-heavy

# Callback functions
## Callback Functions in C
A **callback function** is a function that is **passed as an argument to another function**, and is **called (invoked) inside that function**.
- In C, this is implemented using **function pointers**.
## Why Use Callback Functions?
- To make code **flexible and reusable**
- To allow **custom behavior**
- Common in:
  - Sorting (`qsort`)
  - Event handling
  - Interrupts / drivers
  - Libraries and APIs
## Basic Concept
Instead of hardcoding behavior, you **pass a function** that defines what to do.
## Syntax (Function Pointer)
```c
return_type (*pointer_name)(parameters);
```
## Example 1: Simple Callback
```c
#include <stdio.h>
// callback function
void greet() {
    printf("Hello from callback!\n");
}
// function that takes another function as argument
void execute(void (*func)()) {
    func();  // calling the callback
}
int main() {
    execute(greet);  // passing function as argument
    return 0;
}
```
## Example 2: Callback with Parameters
```c
#include <stdio.h>
int add(int a, int b) {
    return a + b;
}
int multiply(int a, int b) {
    return a * b;
}
// function using callback
void calculate(int x, int y, int (*operation)(int, int)) {
    int result = operation(x, y);
    printf("Result = %d\n", result);
}
int main() {
    calculate(3, 4, add);       // callback to add
    calculate(3, 4, multiply);  // callback to multiply
    return 0;
}
```
## Real-Life Example: Sorting with Callback
C provides `qsort()` where you pass a **comparison function** as a callback.
```c
#include <stdio.h>
#include <stdlib.h>
int compare(const void *a, const void *b) {
    return (*(int*)a - *(int*)b);
}
int main() {
    int arr[] = {5, 2, 8, 1};
    qsort(arr, 4, sizeof(int), compare);
    for(int i = 0; i < 4; i++)
        printf("%d ", arr[i]);
    return 0;
}
```
## How It Works
1. Define a function
2. Pass its address to another function
3. That function calls it using a pointer
## Advantages
- Makes code **modular and flexible**
- Enables **dynamic behavior**
- Reduces code duplication
- Useful in **event-driven systems**
## Summary
- Callback functions allow **functions to call other functions dynamically**
- Achieved using **function pointers**
- Very important concept for **system programming & embedded development**

# Implications on Stack
## Implications of Functions (and Recursion) on the Stack in C
When a function is called in C, it uses a region of memory called the **stack**. Understanding this is important for debugging, performance, and avoiding errors like stack overflow.
## What Happens During a Function Call?
Each function call creates a **stack frame (activation record)** that contains:
- Function parameters
- Local variables
- Return address (where to go back after execution)
- Saved registers (in some cases)
### When the function finishes, its stack frame is removed.
## Stack Behavior (LIFO)
The stack follows **Last In, First Out (LIFO)**:
```
main() → func1() → func2()
Stack:
[func2]
[func1]
[main]
```
When `func2` ends → removed first.
## Example
```c
#include <stdio.h>
void func2() {
    int b = 20;
    printf("In func2\n");
}
void func1() {
    int a = 10;
    func2();
}
int main() {
    func1();
    return 0;
}
```
- Stack flow:
  - `main()` pushed
  - `func1()` pushed
  - `func2()` pushed
  - `func2()` pops → `func1()` → `main()`
## Implications on Stack
### 1. Memory Usage Increases with Function Calls
Each call consumes stack memory.
- eep calls → more memory usage
## 2. Recursion Can Cause Stack Overflow
```c
void fun() {
    fun();  // infinite recursion
}
```
No base case → infinite calls → stack fills → **stack overflow**
## 3. Limited Stack Size
- Stack size is limited (few MBs typically)
- Large local variables can exhaust it
```c
void func() {
    int arr[1000000]; // risky: large stack allocation
}
```
## 4. Automatic Variables are Stored in Stack
- Local variables exist only during function execution
- They are destroyed when function returns
## 5. Function Call Overhead
Each function call:
- Pushes stack frame
- Transfers control
- Pops stack frame
### Too many calls → performance overhead
## 6. Recursion vs Iteration Impact
| Feature     | Recursion             | Iteration |
| ----------- | --------------------- | --------- |
| Stack Usage | High (multiple calls) | Low       |
| Risk        | Stack overflow        | Safe      |
| Performance | Slower                | Faster    |
## 7. Returning Local Variables (Danger)
```c
int* func() {
    int x = 10;
    return &x;  // ❌ invalid (stack memory destroyed)
}
```
Leads to **dangling pointer**
## Stack Overflow
Occurs when:
- Too many function calls (deep recursion)
- Large local variables
- Infinite recursion
## Best Practices
- Always define a **base case** in recursion
- Avoid large local arrays → use **heap** (`malloc`)
- Minimize unnecessary function calls
- Prefer iteration when possible
## Summary
- Each function call creates a **stack frame**
- Stack follows **LIFO**
- Recursion increases stack usage
- Stack is limited → risk of overflow
- Local variables exist only within function scope

# Pass by value/reference
## Pass by Value vs Pass by Reference in C
When you call a function in C, you can pass data in two main ways:
- Pass by Value (default)
- Pass by Reference (using pointers)
## 1. Pass by Value
- A **copy of the variable** is passed to the function.
- Changes inside the function **do NOT affect** the original variable.
### Example
```c
#include <stdio.h>
void change(int x) {
    x = x + 10;
    printf("Inside function: %d\n", x);
}
int main() {
    int a = 5;
    change(a);
    printf("Outside function: %d\n", a);
    return 0;
}
```
### Output
```
Inside function: 15
Outside function: 5
```
Original value remains unchanged
## 2. Pass by Reference (Using Pointers)
- The **address of the variable** is passed
- Function works on the original variable
- Changes **reflect outside**
### Example
```c
#include <stdio.h>
void change(int *x) {
    *x = *x + 10;
}
int main() {
    int a = 5;
    change(&a);
    printf("Outside function: %d\n", a);
    return 0;
}
```
### Output
```
Outside function: 15
```
Original value is modified
## Key Differences
| Feature            | Pass by Value           | Pass by Reference |
| ------------------ | ----------------------- | ----------------- |
| What is passed     | Copy of value           | Address (pointer) |
| Memory             | Extra copy created      | No extra copy     |
| Effect on original | No change               | Changes reflect   |
| Safety             | Safer                   | Needs care        |
| Performance        | Slower (for large data) | Faster            |
## Example: Swap (Most Asked)
### Pass by Value (Fails)
```c
void swap(int a, int b) {
    int temp = a;
    a = b;
    b = temp;
}
```
No effect outside
## Pass by Reference (Works)
```c
void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}
```
## When to Use What?
- Use **Pass by Value**
  - When data should not change
  - For simple variables
- Use **Pass by Reference**
  - When you need to modify original data
  - For large data (arrays, structures)
## Summary
- **Pass by Value** → safe, no modification
- **Pass by Reference** → efficient, allows modification
- C uses **pointers** to achieve reference behavior
