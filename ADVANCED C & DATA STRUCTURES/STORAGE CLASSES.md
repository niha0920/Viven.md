# Scope and lifetime of a variable
In C programming, **scope** and **lifetime (storage duration)** define where a variable can be accessed and how long it exists in memory.
## Scope of a Variable
**Scope** = the region of the program where a variable is accessible.
### 1. Local Scope (Block Scope)
- Declared inside a function or block `{ }`
- Accessible only within that block
```c
#include <stdio.h>
int main() {
    int x = 10;  // local variable
    printf("%d", x);
    return 0;
}
```
- `x` cannot be used outside `main()`
## 2. Global Scope
- Declared outside all functions
- Accessible throughout the program (all functions)
```c
#include <stdio.h>
int x = 20;  // global variable
void display() {
    printf("%d", x);
}
int main() {
    display();
    return 0;
}
```
- `x` is accessible in both `main()` and `display()`
## 3. Function Scope
- Applies only to **labels** (used with `goto`)
- Rarely used
```c
void func() {
    goto label;
    label:
    printf("Hello");
}
```
## 4. File Scope
- Variables declared outside functions
- Accessible from declaration point to end of file
- Can be restricted using `static`
## Lifetime (Storage Duration) of a Variable
**Lifetime** = how long the variable stays in memory.
### 1. Automatic Variables (`auto`)
- Default for local variables
- Created when block starts, destroyed when block ends
```c
void func() {
    int x = 5;  // auto variable
}
```
- Exists only during function execution
## 2. Static Variables
- Retain value between function calls
- Created once, exist till program ends
```c
#include <stdio.h>
void counter() {
    static int count = 0;
    count++;
    printf("%d\n", count);
}
int main() {
    counter();
    counter();
    counter();
}
```
- Output:
```
1
2
3
```
## 3. Register Variables
- Stored in CPU register (faster access)
- Scope same as local variables
```c
void func() {
    register int x = 10;
}
```
- Cannot use `&x` (no memory address guaranteed)
## 4. External Variables (`extern`)
- Used to access global variables from other files
```c
extern int x;
```
## Summary Table
| Type     | Scope          | Lifetime                 |
| -------- | -------------- | ------------------------ |
| Local    | Block          | Till block ends          |
| Global   | Entire program | Entire program execution |
| Static   | Block/File     | Entire program execution |
| Register | Block          | Till block ends          |
| Extern   | Global (files) | Entire program execution |
## Key Difference
- **Scope → Visibility (Where?)**
- **Lifetime → Duration (How long?)**

# Internal
In C, **“internal”** usually refers to **internal linkage**, which is closely related to scope and lifetime.
## Internal Linkage in C
A variable or function has **internal linkage** when it is accessible **only within the same file (source file)** and **not from other files**.
- Achieved using the keyword: `static`
## Example of Internal Linkage
```c
#include <stdio.h>
static int x = 10;  // internal linkage
void display() {
    printf("%d", x);
}
int main() {
    display();
    return 0;
}
```
- `x` can be used anywhere **within this file**
- Cannot be accessed from another file using `extern`
## Internal Linkage for Functions
Functions can also have internal linkage:
```c
#include <stdio.h>
static void show() {
    printf("Hello");
}
int main() {
    show();
}
```
- `show()` is **only visible in this file**
## Internal vs External Linkage
| Feature          | Internal Linkage (`static`) | External Linkage (`extern`) |
| ---------------- | --------------------------- | --------------------------- |
| Visibility       | Within same file            | Across multiple files       |
| Keyword          | `static`                    | `extern`                    |
| Example          | `static int x;`             | `extern int x;`             |
| Access from file | Not allowed                 | Allowed                     |
## Relation with Scope & Lifetime
- **Scope** → File scope (but restricted to one file)
- **Lifetime** → Entire program execution
* Even though it lives throughout the program, it is **hidden from other files**
## Key Point
- Internal linkage = controlled visibility + data hiding
- It is mainly used for:
  - Encapsulation in C
  - Avoiding name conflicts between files
  - Writing modular programs

# External/Global
## External / Global Variables in C
In C, **external variables** (also called **global variables**) are variables declared **outside all functions**. They have **global scope** and typically **external linkage**.
## What is a Global Variable?
A **global variable** is declared outside any function and can be accessed by all functions in the file.
```c
#include <stdio.h>
int x = 100;  // global variable
void show() {
    printf("%d\n", x);
}
int main() {
    show();
    printf("%d", x);
    return 0;
}
- Accessible everywhere in the same file
- Default linkage: **external linkage**
## External Linkage
When a global variable has **external linkage**, it can be accessed **from other files** using the `extern` keyword.
## Example (Multiple Files Concept)
### File1.c
```c
int x = 50;  // definition of global variable
```
### File2.c
```c
#include <stdio.h>
extern int x;  // declaration (not definition)
int main() {
    printf("%d", x);
    return 0;
}
```
- `extern` tells the compiler:
#### “The variable is defined in another file”
## Key Properties
### Scope
- Entire file (from declaration onward)
- Can extend to other files using `extern`
### Lifetime
- Exists for the **entire program execution**
## Important Points
### 1. Declaration vs Definition
- `int x;` → declaration (can also be definition depending on context)
- `extern int x;` → declaration only
- `int x = 10;` → definition
## 2. Default Initialization
- Global variables are automatically initialized to **0**
```c
int x;  // automatically x = 0
```
## 3. Name Conflict
- Two global variables with same name in different files → conflict (unless `static` is used)
## Global vs Local Variable
| Feature       | Global Variable     | Local Variable     |
| ------------- | ------------------- | ------------------ |
| Declaration   | Outside functions   | Inside functions   |
| Scope         | Entire program/file | Inside block only  |
| Lifetime      | Entire program      | Function execution |
| Default Value | 0                   | Garbage value      |
## Key Difference: Internal vs External
| Feature    | Internal (`static`) | External (`global`)   |
| ---------- | ------------------- | --------------------- |
| Visibility | Same file only      | Across files          |
| Linkage    | Internal linkage    | External linkage      |
| Keyword    | `static`            | `extern` (for access) |
## Quick Summary
- **Global variable** = declared outside functions
- **External linkage** = accessible across files
- `extern` = used to access it in another file
- **Lifetime** = entire program
