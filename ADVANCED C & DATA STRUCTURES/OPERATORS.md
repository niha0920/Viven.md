# Binary Operators
## Binary Operators in C
**Binary operators** are operators that work on **two operands** (values or variables). They are one of the most commonly used operator types in C.
## Types of Binary Operators
### 1. Arithmetic Operators
Used for mathematical calculations.
| Operator | Meaning        | Example |
| -------- | -------------- | ------- |
| `+`      | Addition       | a + b   |
| `-`      | Subtraction    | a - b   |
| `*`      | Multiplication | a * b   |
| `/`      | Division       | a / b   |
| `%`      | Modulus        | a % b   |
#### Example:
```c
int a = 10, b = 3;
printf("%d", a + b); // Output: 13
```
## 2. Relational (Comparison) Operators
Used to compare two values.
| Operator | Meaning          |
| -------- | ---------------- |
| `==`     | Equal to         |
| `!=`     | Not equal to     |
| `>`      | Greater than     |
| `<`      | Less than        |
| `>=`     | Greater or equal |
| `<=`     | Less or equal    |
### Example:
```c
if (a > b)
    printf("a is greater");
```
## 3. Logical Operators
Used to combine conditions.
| Operator | Meaning                        | 
| -------- | ------------------------------ | 
| `&&`     | AND                            |   
| `||`     | OR                             |
| `!`      | NOT (unary, but used in logic) |   
### Example:
```c
if (a > 0 && b > 0)
    printf("Both are positive");
```
## 4. Bitwise Operators
Operate at the bit level.
| Operator | Meaning     |    
| -------- | ----------- | 
| `&`      | AND         |    
| `|`      | OR          |
| `^`      | XOR         |   
| `<<`     | Left Shift  |   
| `>>`     | Right Shift |   
### Example:
```c
int x = 5, y = 3;
printf("%d", x & y); // Output: 1
```
## 5. Assignment Operators (Binary form)
Assign values to variables.
| Operator | Example |
| -------- | ------- |
| `=`      | a = b   |
| `+=`     | a += b  |
| `-=`     | a -= b  |
| `*=`     | a *= b  |
| `/=`     | a /= b  |
### Example:
```c
a += b;  // same as a = a + b
```
## Key Points
- Binary operators **require two operands** → `operand1 operator operand2`
- They return a **result value**
- Widely used in expressions, conditions, and computations

# Unary Operators
## Unary Operators in C
**Unary operators** are operators that work on **a single operand** (one variable or value).
## Types of Unary Operators
1. Increment (`++`) and Decrement (`--`)
Used to increase or decrease a value by 1.
### Types:
- **Pre-increment**: `++a` → increment first, then use
- **Post-increment**: `a++` → use first, then increment
#### Example:
```c
int a = 5;
printf("%d", ++a); // Output: 6 (increment first)
printf("%d", a++); // Output: 6 (then becomes 7)
```
## 2. Unary Minus (`-`)
Changes the sign of a value.
### Example:
```c
int a = 5;
printf("%d", -a); // Output: -5
```
## 3. Logical NOT (`!`)
Reverses the logical value.
### Example:
```c
int a = 0;
printf("%d", !a); // Output: 1
```
## 4. Bitwise NOT (`~`)
Flips all bits (1 → 0, 0 → 1).
### Example:
```c
int a = 5; // Binary: 00000101
printf("%d", ~a); // Output: -6
```
## 5. Address-of Operator (`&`)
Gives the **memory address** of a variable.
### Example:
```c
int a = 10;
printf("%p", &a);
```
## 6. Dereference Operator (`*`)
Accesses the value stored at an address (used with pointers).
### Example:
```c
int a = 10;
int *p = &a;
printf("%d", *p); // Output: 10
```
## 7. Sizeof Operator
Returns the size of a variable or data type (in bytes).
### Example:
```c
printf("%lu", sizeof(int)); // Usually 4
```
## Key Points
- Unary operators work on **only one operand**
- Frequently used in **loops, pointers, and expressions**
- Pre and post increment/decrement behave differently → important for interviews

# Ternary Operators
## Ternary Operator in C
The **ternary operator** is the **only operator in C that takes three operands**.
It is a short form of `if-else`.
## Syntax
```c
condition ? expression1 : expression2;
```
- If **condition is true (non-zero)** → `expression1` executes
- If **condition is false (0)** → `expression2` executes
## Example
```c
int a = 10, b = 20;
int max = (a > b) ? a : b;
printf("%d", max); // Output: 20
```
### Equivalent `if-else`:
```c
if (a > b)
    max = a;
else
    max = b;
```
## More Examples
### 1. Even or Odd
```c
int num = 5;
(num % 2 == 0) ? printf("Even") : printf("Odd");
```
## 2. Nested Ternary Operator
```c
int a = 10, b = 20, c = 15;
int max = (a > b) ? 
          ((a > c) ? a : c) : 
          ((b > c) ? b : c);
printf("%d", max); // Output: 20
```
## Key Points
- Compact replacement for **simple if-else**
- Improves readability for **short conditions**
- Avoid using too many nested ternary operators → reduces readability
- Returns a **value**, so it can be used in assignments
## When to Use
- Simple decisions
- Assigning values based on condition
- Avoid for complex logic (use `if-else` instead)

# Special Operators
## Special Operators in C
**Special operators** are a group of operators in C that don’t fall under arithmetic, relational, or logical categories but provide **specific functionalities** like memory access, size calculation, or conditional evaluation.
## Types of Special Operators
### 1. `sizeof` Operator
Returns the **size (in bytes)** of a variable or data type.
#### Example:
```c
int a;
printf("%lu", sizeof(a));     // Output: 4 (depends on system)
printf("%lu", sizeof(float)); // Output: 4
```
## 2. Comma Operator (`,`)
Allows multiple expressions where **only the last value is returned**.
## Example:
```c
int a;
a = (5, 10, 15);
printf("%d", a); // Output: 15
```
## 3. Pointer Operators (`&` and `*`)
Used in pointer operations.
- `&` → Address of variable
- `*` → Value at address (dereference)
### Example:
```c
int a = 10;
int *p = &a;
printf("%p", &a); // address
printf("%d", *p); // value (10)
```
## 4. Member Access Operators (`.` and `->`)
Used with structures.
- `.` → Access member using structure variable
- `->` → Access member using pointer to structure
### Example:
```c
struct Student {
    int age;
};
struct Student s = {20};
struct Student *ptr = &s;
printf("%d", s.age);     // using .
printf("%d", ptr->age);  // using ->
```
## 5. Conditional Operator (`?:`)
Also called **ternary operator** (already discussed).
### Example:
```c
int a = 5, b = 10;
int min = (a < b) ? a : b;
```
## 6. Type Casting Operator
Used to convert one data type into another.
### Example:
```c
int a = 5, b = 2;
float result = (float)a / b;
printf("%f", result); // Output: 2.5
```
## Key Points
- Special operators provide **extra control and flexibility**
- Widely used in **memory handling, structures, and expressions**
- Important for **pointers and system-level programming**

# Order of evaluation
## Order of Evaluation in C (Operator Precedence & Associativity)
In C, when an expression contains multiple operators, the **order of evaluation** determines **which operation is performed first**.
This depends on two things:
- **Operator Precedence** → Priority of operators
- **Associativity** → Direction of evaluation (left-to-right or right-to-left)
## 1. Operator Precedence (High → Low)
| Level | Operators                                                                                          | 
| ----- | -------------------------------------------------------------------------------------------------- | 
| 1     | `()`, `[]`, `->`, `.`                                                                              | 
| 2     | `++`, `--` (unary), `!`, `~`, `+` (unary), `-` (unary), `*` (dereference), `&` (address), `sizeof` | 
| 3     | `*`, `/`, `%`                                                                                      |  
| 4     | `+`, `-`                                                                                           | 
| 5     | `<`, `<=`, `>`, `>=`                                                                               |   
| 6     | `==`, `!=`                                                                                         |  
| 7     | `&` (bitwise AND)                                                                                  |  
| 8     | `^` (bitwise XOR)                                                                                  | 
| 9     | `|` (bitwise OR)                                                                                   |  
| 10    | `&&`                                                                                               |     
| 11    | `||`                                                                                               |   
| 12    | `?:` (ternary)                                                                                     |      
| 13    | `=`, `+=`, `-=`, `*=`, `/=`, `%=`                                                                  |     
| 14    | `,` (comma)                                                                                        |   
## 2. Associativity
| Type                       | Direction    |
| -------------------------- | ------------ |
| Most operators             | Left → Right |
| Unary, Assignment, Ternary | Right → Left |
## 3. Examples
### Example 1
```c
int result = 10 + 5 * 2;
```
Output: `20`
- `*` has higher precedence than `+`
## Example 2
```c
int result = (10 + 5) * 2;
```
Output: `30`
- Parentheses override precedence
## Example 3
```c
int a = 5;
int b = 10;
int c = a > b ? a : b;
```
Output: `10`
## Example 4 (Associativity)
```c
int a = 10 - 5 - 2;
```
Output: `3`
- Evaluated as: `(10 - 5) - 2`
## Example 5
```c
int a = 5;
int b = ++a * 2;
```
Output: `12`
- `++a` happens first → `6 * 2`
## Simple Rule to Remember
- **BODMAS is NOT enough in C**
- Always follow:
1. Parentheses
2. Precedence
3. Associativity
