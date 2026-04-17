# Primitive Data Types
In **C language**, primitive data types (also called **basic data types**) are the fundamental building blocks used to store simple values. They directly represent single data values and are supported by the language by default.
## Main Primitive Data Types in C
### 1. `int` (Integer)
- Used to store **whole numbers** (no decimals)
- Example: `10`, `-25`, `0`
- Memory: Typically **4 bytes** (depends on system)
```c
int a = 10;
```
## 2. `char` (Character)
- Stores a **single character**
- Enclosed in single quotes `' '`
- Internally stored as ASCII value
```c
char ch = 'A';
```
## 3. `float` (Floating Point)
- Stores **decimal numbers** (single precision)
- Memory: **4 bytes**
- Less precision compared to double
```c
float f = 3.14;
```
## 4. `double` (Double Precision)
- Stores **decimal numbers with higher precision**
- Memory: **8 bytes**
```c
double d = 3.1415926535;
```
## 5. `void`
- Represents **no value**
- Used in functions that do not return anything
```c
void display() {
    // no return value
}
```
## Modifiers of Primitive Data Types
These modify the size or sign of basic data types:
| Modifier   | Example      |
| ---------- | ------------ |
| `short`    | short int    |
| `long`     | long int     |
| `signed`   | signed int   |
| `unsigned` | unsigned int |
```c
unsigned int x = 100;
long int y = 123456789;
```
## Summary Table
| Data Type | Description              | Example |
| --------- | ------------------------ | ------- |
| int       | Integer values           | 10      |
| char      | Single character         | 'A'     |
| float     | Decimal (low precision)  | 3.14    |
| double    | Decimal (high precision) | 3.14159 |
| void      | No value                 | —       |
## Key Points
- Primitive types are **built-in** and **basic**
- Used to construct complex data types (arrays, structures, etc.)
- Memory size may vary depending on compiler/system

# Aggregated Data Types
In **C language**, Aggregated Data Types (also called **derived** or **composite data types**) are types that **combine multiple primitive data elements** into a single unit.
They help organize related data and are widely used in real-world programming.
## Types of Aggregated Data Types in C
### 1. Array
- Collection of **same type elements**
- Stored in **contiguous memory locations**
- Accessed using index
```c
int arr[5] = {1, 2, 3, 4, 5};
```
#### Example:
- `arr[0] = 1`
- `arr[4] = 5`
## 2. Structure (`struct`)
- Collection of **different data types**
- Groups related variables
```c
struct Student {
    int id;
    char name[20];
    float marks;
};
```
### Access:
```c
struct Student s1;
s1.id = 1;
```
## 3. Union (`union`)
- Similar to structure, but **shares memory**
- Only **one member is active at a time**
```c
union Data {
    int i;
    float f;
};
```
### Key point:
- All members use **same memory location**
## 4. Enumeration (`enum`)
- User-defined type with **named integer constants**
```c
enum Day {MON, TUE, WED, THU, FRI};
```
### Default values:
- `MON = 0`, `TUE = 1`, etc.
## Summary Table
| Type      | Description               | Key Feature          |
| --------- | ------------------------- | -------------------- |
| Array     | Same data type collection | Indexed access       |
| Structure | Different data types      | Separate memory      |
| Union     | Different data types      | Shared memory        |
| Enum      | Named constants           | Improves readability |
## Key Differences
| Feature | Structure                | Union                  |
| ------- | ------------------------ | ---------------------- |
| Memory  | Separate for each member | Shared                 |
| Size    | Sum of all members       | Size of largest member |
| Usage   | Store multiple values    | Save memory            |
## Key Points
- Aggregated types are used to **group related data**
- Help in building **complex programs**
- Essential for **data structures (like linked lists, trees, etc.)**
