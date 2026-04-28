# Defining, initializing and using arrays
Arrays are one of the most important concepts in C programming. Let’s break it down clearly into **definition, initialization, and usage** so you can understand it step by step.
## 1. Defining an Array
An **array** is a collection of elements of the same data type stored in contiguous memory locations.
### Syntax:
```c
data_type array_name[size];
```
### Example:
```c
int arr[5];
```
- This creates an array named `arr` that can store **5 integers**
- Index starts from **0 to 4**
## 2. Initializing an Array
Initialization means assigning values to the array.
### Method 1: During Declaration
```c
int arr[5] = {10, 20, 30, 40, 50};
```
### Method 2: Without Size (Compiler decides size)
```c
int arr[] = {1, 2, 3, 4};
```
### Method 3: Partial Initialization
```c
int arr[5] = {10, 20};
```
- Remaining elements will be initialized to **0**
## 3. Accessing (Using) Array Elements
Array elements are accessed using **index (subscript)**.
### Example:
```c
int arr[3] = {5, 10, 15};
printf("%d", arr[0]); // Output: 5
printf("%d", arr[1]); // Output: 10
```
## 4. Using Arrays with Loops
Instead of accessing one by one, we use loops.
### Example:
```c
#include <stdio.h>
int main() {
    int arr[5] = {1, 2, 3, 4, 5};
    for(int i = 0; i < 5; i++) {
        printf("%d ", arr[i]);
    }
    return 0;
}
```
- Output:
```
1 2 3 4 5
```
## 5. Taking Input into Array
```c
#include <stdio.h>
int main() {
    int arr[5];
    for(int i = 0; i < 5; i++) {
        scanf("%d", &arr[i]);
    }
    for(int i = 0; i < 5; i++) {
        printf("%d ", arr[i]);
    }
    return 0;
}
```
## 6. Important Points
- Index always starts from **0**
- Array size is fixed (cannot change later)
- All elements must be of **same data type**
- Stored in **contiguous memory**
## 7. Types of Arrays (Brief)
- **1D Array** → `int arr[5];`
- **2D Array** → `int arr[3][3];`
- **Multi-dimensional Array**
## Quick Summary
- **Define** → `int arr[5];`
- **Initialize** → `int arr[5] = {1,2,3,4,5};`
- **Use** → Access with `arr[i]`

# Multi Dimensional arrays
Multi-dimensional arrays are a natural extension of 1D arrays—very important in C, especially for matrices and tables. Let’s build it step by step so it’s easy to understand.
## 1. What is a Multi-Dimensional Array?
A **multi-dimensional array** is an array of arrays.
- Used to represent:
  - Tables
  - Matrices
  - Grids
- Most common: **2D array**
## 2. Defining a 2D Array
### Syntax:
```c
data_type array_name[rows][columns];
```
### Example:
```c
int arr[3][4];
```
- 3 rows and 4 columns
- Total elements = 3 × 4 = 12
## 3. Visual Representation
Think of it like a table:
```
arr[3][4]
Row\Col   0    1    2    3
        --------------------
0       | a00  a01  a02  a03
1       | a10  a11  a12  a13
2       | a20  a21  a22  a23
```
## 4. Initializing a 2D Array
### Method 1: Full Initialization
```c
int arr[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
```
### Method 2: Flat Initialization
```c
int arr[2][3] = {1, 2, 3, 4, 5, 6};
```
### Method 3: Without Row Size
```c
int arr[][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
```
## 5. Accessing Elements
### Syntax:
```c
arr[row][column]
```
### Example:
```c
printf("%d", arr[1][2]);  // Output: 6
```
## 6. Using Loops (Very Important)
We use **nested loops**.
### Example:
```c
#include <stdio.h>
int main() {
    int arr[2][3] = {
        {1, 2, 3},
        {4, 5, 6}
    };
    for(int i = 0; i < 2; i++) {
        for(int j = 0; j < 3; j++) {
            printf("%d ", arr[i][j]);
        }
        printf("\n");
    }
    return 0;
}
```
- Output:
```
1 2 3
4 5 6
```
## 7. Taking Input for 2D Array
```c
int arr[2][3];
for(int i = 0; i < 2; i++) {
    for(int j = 0; j < 3; j++) {
        scanf("%d", &arr[i][j]);
    }
}
```
## 8. Memory Representation (Important for Exams)
- Stored in **row-major order** in C
### That means:
```
arr[0][0], arr[0][1], arr[0][2], ...
then next row
```
## 9. 3D Array (Brief Idea)
### Syntax:
```c
int arr[2][3][4];
```
- Think of it as multiple 2D arrays stacked together
## 10. Real-Life Uses
- Matrix operations
- Image processing (pixels)
- Game boards (chess, tic-tac-toe)
- Tables/data storage
## Quick Summary
- 2D array → `int arr[rows][cols];`
- Access → `arr[i][j]`
- Use nested loops
- Stored in row-major order

# Arrays of Characters and Strings
Arrays of characters are how **strings** are handled in C. This is a very important topic because C does not have a built-in string type like some other languages.
## 1. Character Arrays
A **character array** is simply an array of char values.
### Example:
```c
char name[5] = {'H', 'e', 'l', 'l', 'o'};
```
- This is **NOT a string** (no null character `\0`)
- Just a collection of characters
## 2. Strings in C
A **string** is a character array that ends with a **null character** `\0`.
### Example:
```c
char name[6] = {'H', 'e', 'l', 'l', 'o', '\0'};
```
- `\0` marks the **end of the string**
## 3. String Initialization (Easy Way)
Instead of writing `\0` manually:
```c
char name[] = "Hello";
```
- Compiler automatically adds `\0`
- Size becomes **6 (5 + 1)**
## 4. Memory Representation
```
Index:   0   1   2   3   4   5
Value:  'H' 'e' 'l' 'l' 'o' '\0'
```
## 5. Accessing Characters
```c
char name[] = "Hello";
printf("%c", name[0]);  // H
printf("%c", name[1]);  // e
```
## 6. Input and Output of Strings
### Using `scanf`
```
char name[20];
scanf("%s", name);
```
- Stops at **space**
### Using `fgets` (Better)
```c
char name[20];
fgets(name, sizeof(name), stdin);
```
- Reads full line including spaces
## Output using `printf`
```c
printf("%s", name);
```
## 7. Common String Functions
From the string.h library:
### `strlen()` → Length of string
```c
strlen(name);
```
### `strcpy()` → Copy string
```c
strcpy(dest, src);
```
### `strcat()` → Concatenate
```c
strcat(str1, str2);
```
### strcmp() → Compare
```c
strcmp(str1, str2);
```
## 8. Example Program
```c
#include <stdio.h>
#include <string.h>
int main() {
    char name[20];
    printf("Enter name: ");
    fgets(name, sizeof(name), stdin);
    printf("You entered: %s", name);
    return 0;
}
```
## 9. Difference: Character Array vs String
| Feature   | Character Array | String          |
| --------- | --------------- | --------------- |
| Null `\0` | Not required    | Required        |
| Meaning   | Just characters | Meaningful text |
| Example   | `{'H','i'}`     | `"Hi"`          |
## Quick Summary
- **Character array** → collection of chars
- **String** → char array + `\0`
- Use `"Hello"` instead of manual initialization
- Use `<string.h>` functions

# Arrays and pointers
Understanding the relationship between **arrays and pointers in C** is crucial—it’s one of the most tested and most misunderstood topics. Let’s break it down clearly and practically.
## 1. Basic Idea
In C, an **array name behaves like a pointer** to its first element.
### Example:
```c
int arr[5] = {10, 20, 30, 40, 50};
```
- `arr` → address of `arr[0]`
- So:
```
arr == &arr[0]
```
## 2. Accessing Elements (Two Ways)
### Using Array Index
```c
arr[2]   // 30
```
### Using Pointer
```c
*(arr + 2)   // 30
```
- Both are **equivalent**
## 3. Visual Understanding
<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/71ca43bf-9293-4078-963d-9ed72e5554a6" />

- Each step (`arr + 1`) moves by **size of data type**
- If `int` = 4 bytes → next address jumps by 4 bytes
## 4. Pointer Arithmetic
```c
int *p = arr;
```
| Expression | Meaning                  |
| ---------- | ------------------------ |
| `p`        | address of first element |
| `p + 1`    | address of next element  |
| `*(p + 1)` | value of next element    |
## 5. Arrays as Function Arguments
When you pass an array to a function, it behaves like a pointer.
### Example:
```c
void printArray(int arr[], int n) {
    for(int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
}
```
- Internally treated as:
```c
void printArray(int *arr, int n);
```
## 6. Key Difference: Array vs Pointer
| Feature    | Array                     | Pointer            |
| ---------- | ------------------------- | ------------------ |
| Memory     | Fixed size                | Can point anywhere |
| Assignment | Not allowed (`arr = p`)   | Allowed            |
| Increment  | Not allowed (`arr++`)     | Allowed            |
## 7. Important Example
```c
int arr[3] = {10, 20, 30};
int *p = arr;
printf("%d\n", arr[1]);     // 20
printf("%d\n", *(p + 1));   // 20
```
## 8. Special Case: `&arr`
```c
int arr[5];
```
- `arr` → pointer to first element → `int *`
- `&arr` → pointer to whole array → `int (*)[5]`
* Subtle but important difference in advanced C
## 9. Pointer Traversal of Array
```c
int *p = arr;
for(int i = 0; i < 5; i++) {
    printf("%d ", *(p + i));
}
```
## Quick Summary
- Array name → pointer to first element
- `arr[i]` ↔ `*(arr + i)`
- Arrays ≠ pointers (important difference)
- Arrays passed to functions behave like pointers

# Passing arrays to functions
Passing arrays to functions in C is a key concept—and a bit tricky because arrays **decay into pointers** when passed. Let’s go step by step so it’s clear.
## 1. Basic Idea
When you pass an array to a function, you are actually passing the **address of its first element**.
```c
int arr[5] = {1, 2, 3, 4, 5};
```
Passing:
```c
func(arr);
```
- is equivalent to:
```
func(&arr[0]);
```
## 2. Function Declaration Ways
All three below are **equivalent**:
```c
void func(int arr[]);
void func(int arr[5]);
void func(int *arr);
```
- Internally, all are treated as:
```c
void func(int *arr);
```
## 3. Example Program
```c
#include <stdio.h>
void printArray(int arr[], int n) {
    for(int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
}
int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    printArray(arr, 5);
    return 0;
}
```
- Output:
```
10 20 30 40 50
```
## 4. Why Size Must Be Passed
Inside the function, array size is **not known**.
```c
sizeof(arr)   // gives size of pointer, NOT array
```
- So always pass size explicitly:
```c
func(arr, size);
```
## 5. Modifying Array in Function
Since we pass the address, changes reflect in the original array.
### Example:
```c
#include <stdio.h>
void modify(int arr[], int n) {
    arr[0] = 100;
}
int main() {
    int arr[3] = {1, 2, 3};
    modify(arr, 3);
    printf("%d", arr[0]);  // Output: 100
}
```
- This is like **pass by reference behavior**
## 6. Using Pointer Notation
```c
void func(int *arr, int n) {
    for(int i = 0; i < n; i++) {
        printf("%d ", *(arr + i));
    }
}
```
- Same as `arr[i]`
## 7. Passing 2D Arrays
Here, things are stricter.
### Example:
```c
void func(int arr[][3], int rows);
```
- Column size must be specified
## Example Program:
```c
#include <stdio.h>
void print2D(int arr[][3], int rows) {
    for(int i = 0; i < rows; i++) {
        for(int j = 0; j < 3; j++) {
            printf("%d ", arr[i][j]);
        }
        printf("\n");
    }
}
int main() {
    int arr[2][3] = {{1,2,3},{4,5,6}};
    print2D(arr, 2);
}
```
## 8. Common Mistake 
```c
void func(int arr[]) {
    int size = sizeof(arr)/sizeof(arr[0]);  // WRONG
}
```
- Because `arr` is treated as pointer
## Quick Summary
- Array → passed as pointer
- `arr` ≡ `&arr[0]`
- Must pass size
- Changes reflect back

# String handling and its library functions
String handling in C revolves around **character arrays terminated by** `'\0'` and a rich set of helper functions from the standard library header string.h. Here’s a clear, exam-focused guide.
## 1. What is a String in C?
A string is:
```c
char str[] = "Hello";
```
- Internally stored as:
```
'H' 'e' 'l' 'l' 'o' '\0'
```
- `'\0'` (null terminator) marks the end of the string.
## 2. Common String Operations
- Finding length
- Copying
- Concatenation
- Comparing
- Searching
### All are supported by functions in `<string.h>`.
## 3. Important String Library Functions
### 1. `strlen()` – Length of String
```c
#include <string.h>
int len = strlen("Hello");  // 5
```
- Counts characters **excluding** `\0`
### 2. `strcpy()` – Copy String
```c
char src[] = "Hello";
char dest[10];
strcpy(dest, src);
```
- Copies entire string (including `\0`)
### 3. `strcat()` – Concatenate Strings
```c
char s1[20] = "Hello ";
char s2[] = "World";
strcat(s1, s2);
```
- Result: `"Hello World"`
## 4. `strcmp()` – Compare Strings
```c
strcmp("abc", "abc");  // 0
strcmp("abc", "abd");  // < 0
strcmp("abd", "abc");  // > 0
```
- Returns:
- `0` → equal
- negative → first < second
- positive → first > second
## 5. `strchr()` – Find Character
```c
char *p = strchr("Hello", 'l');
```
- Returns pointer to first occurrence
## 6. `strstr()` – Find Substring
```c
char *p = strstr("Hello World", "World");
```
- Returns pointer to substring
## 4. Example Program
```c
#include <stdio.h>
#include <string.h>
int main() {
    char s1[20] = "Hello";
    char s2[] = " World";
    strcat(s1, s2);
    printf("Concatenated: %s\n", s1);
    printf("Length: %lu\n", strlen(s1));
    return 0;
}
```
## 5. Input / Output of Strings
### Input
```c
char str[20];
scanf("%s", str);      // stops at space
fgets(str, 20, stdin); // reads full line
```
### Output
```c
printf("%s", str);
```
## 6. Important Points 
- Strings are **arrays of characters**
- Must end with `'\0'`
- Functions in `<string.h>` do **not check bounds**
- Destination array must be large enough
## 7. Common Mistakes 
### Missing space for `\0`
```c
char str[5] = "Hello"; // WRONG
```
### Using `=` for strings
```c
str1 = str2; // INVALID
```
- Use `strcpy()` instead
## 8. Useful Variants (Safer Functions)
- `strncpy()` – limited copy
- `strncat()` – limited concatenate
- `strncmp()` – limited compare
## Quick Summary
- Strings = `char[] + '\0'`
- Use `<string.h>` functions
- `strlen`, `strcpy`, `strcat`, `strcmp` are most important
- Always ensure enough memory
