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
