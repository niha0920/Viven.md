# Usage of Structures
Structures in **C programming** are a powerful feature used to group different types of data into a single unit. They are widely used in real-world applications where multiple related variables need to be handled together.
## What is a Structure?
A **structure** (`struct`) is a user-defined data type that allows you to combine variables of **different data types** under one name.
### Example:
```c
struct Student {
    int id;
    char name[50];
    float marks;
};
```
## Usage of Structures
### 1. Grouping Related Data
Structures help in organizing related data logically.
```c
struct Student s1;
s1.id = 101;
strcpy(s1.name, "Niharika");
s1.marks = 95.5;
```
- Instead of separate variables, all student-related data is stored together.
## 2. Creating Complex Data Types
Structures allow creation of customized data types.
```c
struct Point {
    int x;
    int y;
};
```
Used in graphics, coordinate systems, etc.
## 3. Arrays of Structures
Used when handling multiple records.
```c
struct Student s[3];
```
### Useful in:
- Student databases
- Employee records
- Inventory systems
## 4. Structures with Pointers
Pointers can be used to access structures efficiently.
```c
struct Student *ptr;
ptr = &s1;
printf("%d", ptr->id);
```
- Useful for dynamic memory and efficient data handling.
## 5. Nested Structures
Structures can be inside other structures.
```c
struct Date {
    int day, month, year;
};
struct Student {
    int id;
    struct Date dob;
};
```
- Helps represent complex relationships.
## 6. Passing Structures to Functions
### By Value:
```c
void display(struct Student s);
```
###  By Reference:
```c
void display(struct Student *s);
```
- Passing by reference is more efficient.
## 7. File Handling with Structures
Structures are used to store and retrieve records from files.
```c
fwrite(&s1, sizeof(s1), 1, fp);
```
- Used in databases and persistent storage.
## 8. Self-Referential Structures
Used in data structures like linked lists.
```c
struct Node {
    int data;
    struct Node *next;
};
```
### Important for:
- Linked lists
- Trees
- Graphs
## Advantages of Structures
- Organizes complex data
- Improves code readability
- Supports real-world modeling
- Enables data abstraction
## Real-Time Applications
- Student Management Systems
- Banking Systems
- Operating Systems
- Networking (packet structures)
- Embedded systems
## Key Points to Remember
- Use `.` operator for variables
- Use `->` operator for pointers
- Structures can be combined with arrays, pointers, and functions

# Declaration, initialization and accessing
## 1. Declaration of Structure
Structure declaration defines the format (template), not actual memory.
```c
struct Student {
    int id;
    char name[50];
    float marks;
};
```
- This only tells the compiler what a `Student` looks like.
## Creating Structure Variables
```c
struct Student s1, s2;
```
- Now memory is allocated for `s1` and `s2`.
## 2. Initialization of Structure
### Method 1: At the time of declaration
```c
struct Student s1 = {101, "Niharika", 95.5};
```
- Values are assigned in the same order as members.
### Method 2: Partial Initialization
```c
struct Student s2 = {102, "Rahul"};
```
- Remaining values will be default (0 or garbage depending on context).
### Method 3: Using Designated Initialization (C99)
```c
struct Student s3 = {
    .name = "Anjali",
    .id = 103,
    .marks = 88.0
};
```
- Order doesn’t matter here.
### Method 4: Runtime Initialization
```c
struct Student s4;
s4.id = 104;
strcpy(s4.name, "Kiran");
s4.marks = 91.2;
```
## 3. Accessing Structure Members
### Using Dot (`.`) Operator
```c
printf("%d", s1.id);
printf("%s", s1.name);
printf("%f", s1.marks);
```
- Used when working with structure variables.
### Using Arrow (`->`) Operator (Pointers)
```c
struct Student *ptr = &s1;
printf("%d", ptr->id);
printf("%s", ptr->name);
printf("%f", ptr->marks);
```
- Used when accessing via pointer.
## Complete Example Program
```c
#include <stdio.h>
#include <string.h>
struct Student {
    int id;
    char name[50];
    float marks;
};
int main() {
    struct Student s1 = {101, "Niharika", 95.5};
    struct Student s2;
    s2.id = 102;
    strcpy(s2.name, "Rahul");
    s2.marks = 88.0;
    printf("Student 1: %d %s %.2f\n", s1.id, s1.name, s1.marks);
    printf("Student 2: %d %s %.2f\n", s2.id, s2.name, s2.marks);
    return 0;
}
```
## Key Points
- **Declaration** → Defines structure format
- **Initialization** → Assigns values
- **Accessing** → Uses `.` or `->`

# Nested Structures
## Nested Structures in C
A **nested structure** is a structure that contains another structure as one of its members. This helps represent **complex real-world data** in a clean and organized way.
## 1. Basic Concept
Instead of keeping everything in one structure, we divide related data into smaller structures and **embed them inside another structure**.
## Example: Student with Date of Birth
```c
struct Date {
    int day;
    int month;
    int year;
};
struct Student {
    int id;
    char name[50];
    struct Date dob;   // Nested structure
};
```
- Here, `Date` is nested inside `Student`.
## 2. Initialization of Nested Structures
```c
struct Student s1 = {101, "Niharika", {15, 8, 2003}};
```
- Inner braces `{15, 8, 2003}` initialize the nested structure.
## 3. Accessing Nested Structure Members
Use **dot operator** (`.`) multiple times.
```c
printf("%d", s1.dob.day);
printf("%d", s1.dob.month);
printf("%d", s1.dob.year);
```
- Format:
```
structure_variable.nested_structure.member
```
## 4. Using Pointers with Nested Structures
```c
struct Student *ptr = &s1;
printf("%d", ptr->dob.day);
```
- You can combine `->` and `.` operators.
## 5. Complete Program Example
```c
#include <stdio.h>
#include <string.h>
struct Date {
    int day, month, year;
};
struct Student {
    int id;
    char name[50];
    struct Date dob;
};
int main() {
    struct Student s1 = {101, "Niharika", {15, 8, 2003}};
    printf("ID: %d\n", s1.id);
    printf("Name: %s\n", s1.name);
    printf("DOB: %d-%d-%d\n", s1.dob.day, s1.dob.month, s1.dob.year);
    return 0;
}
```
## 6. Why Use Nested Structures?
- Better organization of data
- Improves readability
- Represents real-world relationships
- Makes programs modular
## 7. Real-Life Examples
- Student → Date of Birth
- Employee → Address (street, city, zip)
- Bank Account → Customer Details
- Network Packet → Header + Data
## Key Points
- A structure can contain another structure
- Access using `.` or `->`
- Initialization uses **nested braces** `{}`
- Helps model complex data easily

# Array of structures
## Array of Structures in C
An **array of structures** is a collection of multiple structure variables of the same type, stored in contiguous memory locations. It is used when you need to handle **multiple records** (like many students, employees, etc.).
## 1. Declaration of Array of Structures
```c
struct Student {
    int id;
    char name[50];
    float marks;
};
struct Student s[3];   // Array of 3 students
```
- `s[0]`, `s[1]`, `s[2]` are individual structure variables.
## 2. Initialization of Array of Structures
### Method 1: At Declaration
```c
struct Student s[3] = {
    {101, "Niharika", 95.5},
    {102, "Rahul", 88.0},
    {103, "Anjali", 91.2}
};
```
## Method 2: Runtime Initialization (Using Loop)
```c
for(int i = 0; i < 3; i++) {
    printf("Enter id, name, marks: ");
    scanf("%d %s %f", &s[i].id, s[i].name, &s[i].marks);
}
```
## 3. Accessing Elements
Use **index + dot operator** (`.`)
```c
printf("%d", s[0].id);
printf("%s", s[1].name);
printf("%f", s[2].marks);
```
## 4. Using Pointers with Array of Structures
```c
struct Student *ptr = s;
printf("%d", (ptr + 1)->id);
```
- `(ptr + i)->member` accesses ith element.
## 5. Complete Example Program
```c
#include <stdio.h>
#include <string.h>
struct Student {
    int id;
    char name[50];
    float marks;
};
int main() {
    struct Student s[3];
    for(int i = 0; i < 3; i++) {
        printf("Enter details of student %d:\n", i + 1);
        scanf("%d %s %f", &s[i].id, s[i].name, &s[i].marks);
    }
    printf("\nStudent Details:\n");
    for(int i = 0; i < 3; i++) {
        printf("%d %s %.2f\n", s[i].id, s[i].name, s[i].marks);
    }
    return 0;
}
```
## 6. Advantages
- Stores multiple records efficiently
- Easy to process using loops
- Useful in real-world applications
- Improves code organization
## 7. Real-Time Applications
- Student database
- Employee records
- Library systems
- Banking systems
- Inventory management
## Key Points to Remember
- Access using: `array[index].member`
- Works well with loops
- Can be combined with:
  - Pointers
  - Functions
  - File handling

# Allocation of memory and holes
## Allocation of Memory and Holes in Structures (C)
When you use structures in C, memory is allocated for each member—but not always in a simple continuous way. Due to **alignment requirements**, the compiler may introduce **holes (padding bytes)**.
## 1. Memory Allocation in Structures
Each member of a structure is stored in memory, typically in the **order of declaration**.
### Example:
```c
struct Example {
    int a;     // 4 bytes
    char b;    // 1 byte
    float c;   // 4 bytes
};
```
- You might expect size = **4 + 1 + 4 = 9 bytes**,
####
but actual size is usually **12 bytes**
## 2. What are “Holes” (Padding)?
**Holes** are unused bytes inserted by the compiler to ensure proper **memory alignment**.
- Why?
Processors access data faster when it is aligned (e.g., 4-byte data at addresses divisible by 4).
## Memory Layout Example
```c
struct Example {
    int a;
    char b;
    float c;
};
```
### Typical Layout in Memory:
```
a → [4 bytes]
b → [1 byte]
padding → [3 bytes]  ← hole
c → [4 bytes]
```
- Total = **12 bytes**
## 3. Another Example (More Holes)
```c
struct Test {
    char a;   // 1 byte
    int b;    // 4 bytes
    char c;   // 1 byte
};
```
### Layout:
```
a → [1 byte]
padding → [3 bytes]
b → [4 bytes]
c → [1 byte]
padding → [3 bytes]
```
- Total = **12 bytes** (not 6)
## 4. Structure Alignment Rule
- Each data type has an **alignment requirement**
- Compiler adds padding so that:
  - `int` starts at multiple of 4
  - `double` starts at multiple of 8 (on many systems)
###
Structure size = multiple of **largest data type alignment**
## 5. Reducing Holes (Optimization)
Reorder members from **largest → smallest**.
### Poor Design:
```c
struct Bad {
    char a;
    int b;
    char c;
};
```
### Optimized Design:
```c
struct Good {
    int b;
    char a;
    char c;
};
```
- Size reduces (e.g., from 12 → 8 bytes)
## 6. Checking Structure Size
Use `sizeof()`:
```c
printf("%lu", sizeof(struct Example));
```
## 7. Important Notes
- Padding depends on compiler & architecture
- Improves performance (not memory efficiency)
- Cannot always be avoided completely
- Important in:
  - Embedded systems
  - Networking (packet structures)
  - Memory-critical applications
## 8. Packed Structures (Advanced)
To remove padding:
```c
#pragma pack(1)
struct Packed {
    char a;
    int b;
};
```
- No holes, but may reduce performance.
## Key Points
- **Memory is not always tightly packed**
- **Holes = padding bytes added for alignment**
- **Reordering members reduces memory waste**
- **Alignment improves CPU performance**

# Unions
## Unions in C
A **union** is a user-defined data type (like a structure) that allows you to store **different data types in the same memory location**.
- Key idea:
### 
**All members share the same memory** → only **one member can hold a valid value at a time**.
## 1. Declaration of Union
```c
union Data {
    int i;
    float f;
    char str[20];
};
```
## 2. Creating Union Variables
```c
union Data d1;
```
## 3. Memory Allocation in Union
Unlike structures, **union allocates memory equal to its largest member**.
### Example:
```c
union Data {
    int i;       // 4 bytes
    float f;     // 4 bytes
    char str[20];// 20 bytes
};
```
- Total size = **20 bytes** (not 28)
## 4. Initialization of Union
```c
union Data d1 = {10};   // Initializes first member (i)
```
- Only **one member can be initialized at a time**.
## 5. Accessing Union Members
```c
d1.i = 10;
printf("%d\n", d1.i);
d1.f = 3.14;
printf("%f\n", d1.f);
```
- When you assign a new value, previous data is **overwritten**.
## 6. Demonstration of Shared Memory
```c
#include <stdio.h>
union Data {
    int i;
    float f;
};
int main() {
    union Data d;
    d.i = 10;
    printf("i = %d\n", d.i);
    d.f = 3.14;
    printf("f = %f\n", d.f);
    printf("i (after f assigned) = %d\n", d.i);
    return 0;
}
```
- Output shows that changing `f` affects `i`.
## 7. Structure vs Union (Quick Difference)
| Feature | Structure                     | Union                     |
| ------- | ----------------------------- | ------------------------- |
| Memory  | Separate for each member      | Shared memory             |
| Size    | Sum of all members (+padding) | Size of largest member    |
| Usage   | Store multiple values         | Store one value at a time |
| Access  | All members valid             | Only last assigned valid  |
## 8. Use Cases of Unions
- Memory optimization
- Embedded systems
- Hardware registers
- Interpreting same data in different formats
- Variant data (like one variable holding multiple types)
## 9. Example Use Case
```c
union Value {
    int intVal;
    float floatVal;
};
union Value v;
v.intVal = 5;
v.floatVal = 3.5;  // overwrites intVal
```
## 10. Important Points
- Only one member is valid at a time
- All members share the same memory address
- Changing one member affects others
- Used when memory efficiency is critical
## Key Takeaway
- **Structure = “store everything”**
- **Union = “store one at a time efficiently”**
