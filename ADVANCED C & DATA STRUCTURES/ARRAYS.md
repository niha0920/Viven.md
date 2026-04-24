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
