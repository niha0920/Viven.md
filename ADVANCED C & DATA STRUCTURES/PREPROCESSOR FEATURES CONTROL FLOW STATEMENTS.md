# The Control Flow Program Statements
Control flow statements in C determine the **order in which statements are executed** in a program. Normally, execution happens sequentially (top to bottom), but control flow statements allow you to **change that flow** based on conditions, loops, or jumps.
## Types of Control Flow Statements in C
### 1. Decision-Making Statements (Selection)
These statements allow the program to **make decisions based on conditions**.
#### `if` Statement
Executes a block only if the condition is true.
```c
if (x > 0) {
    printf("Positive number");
}
```
## `if-else`
Chooses between two blocks.
```c
if (x % 2 == 0) {
    printf("Even");
} else {
    printf("Odd");
}
```
## `else if` Ladder
Used when multiple conditions exist.
```c
if (marks >= 90) {
    printf("Grade A");
} else if (marks >= 75) {
    printf("Grade B");
} else {
    printf("Grade C");
}
```
## `switch` Statement
Used for multiple choices based on a single variable.
```c
switch (day) {
    case 1: printf("Monday"); break;
    case 2: printf("Tuesday"); break;
    default: printf("Invalid");
}
```
## 2. Looping Statements (Iteration)
Used to **repeat a block of code multiple times**.
## `for` Loop
Best when the number of iterations is known.
```c
for (int i = 0; i < 5; i++) {
    printf("%d ", i);
}
```
## `while` Loop
Executes while condition is true.
```c
int i = 0;
while (i < 5) {
    printf("%d ", i);
    i++;
}
```
## `do-while` Loop
Executes **at least once**, even if condition is false.
```c
int i = 0;
do {
    printf("%d ", i);
    i++;
} while (i < 5);
```
## 3. Jump Statements
Used to **alter the flow abruptly**.
## `break`
Terminates loop or switch.
```c
for (int i = 0; i < 10; i++) {
    if (i == 5)
        break;
}
```
## `continue`
Skips current iteration and moves to next.
```c
for (int i = 0; i < 5; i++) {
    if (i == 2)
        continue;
    printf("%d ", i);
}
```
## `goto`
Transfers control to a labeled statement (generally discouraged).
```c
goto label;
label:
printf("Jumped here");
```
## `return`
Exits from a function.
```c
return 0;
```
## Summary Table
| Type     | Statements                    | Purpose               |
| -------- | ----------------------------- | --------------------- |
| Decision | if, if-else, switch           | Conditional execution |
| Looping  | for, while, do-while          | Repetition            |
| Jump     | break, continue, goto, return | Change flow instantly |

# Looping Statements
Looping statements in C are used to **execute a block of code repeatedly** until a specified condition is met. They are essential for tasks like iterating through arrays, repeating calculations, or processing input.
## Types of Looping Statements in C
### 1. `for` Loop (Entry-Controlled Loop)
Used when the **number of iterations is known in advance**.
##### Syntax
```c
for (initialization; condition; increment/decrement) {
    // body
}
```
#### Example
```c
for (int i = 1; i <= 5; i++) {
    printf("%d ", i);
}
```
#### Flow
- Initialize → Check condition → Execute → Update → Repeat
## 2. `while` Loop (Entry-Controlled Loop)
Used when the **number of iterations is not known beforehand**.
### Syntax
```c
while (condition) {
    // body
}
```
### Example
```c
int i = 1;
while (i <= 5) {
    printf("%d ", i);
    i++;
}
```
### Flow
- Check condition → Execute → Update → Repeat
## 3. `do-while` Loop (Exit-Controlled Loop)
Executes the loop body **at least once**, even if the condition is false.
### Syntax
```c
do {
    // body
} while (condition);
```
### Example
```c
int i = 1;
do {
    printf("%d ", i);
    i++;
} while (i <= 5);
```
### Flow
- Execute → Check condition → Repeat if true
## Key Differences
| Feature         | `for` Loop       | `while` Loop       | `do-while` Loop        |
| --------------- | ---------------- | ------------------ | ---------------------- |
| Control Type    | Entry-controlled | Entry-controlled   | Exit-controlled        |
| Condition Check | Before execution | Before execution   | After execution        |
| Minimum Runs    | 0                | 0                  | 1                      |
| Use Case        | Known iterations | Unknown iterations | Must run at least once |
## Example Comparison
```c
// for loop
for (int i = 0; i < 3; i++)
    printf("For\n");
// while loop
int i = 0;
while (i < 3) {
    printf("While\n");
    i++;
}
// do-while loop
int j = 0;
do {
    printf("Do-While\n");
    j++;
} while (j < 3);
```

# The Data-Checking Process
The **Data-Checking Process in C** refers to the techniques used to **validate input data before processing it**, ensuring correctness, reliability, and preventing errors during execution.
## What is Data Checking?
It is the process of verifying that:
- Input is **valid**
- Data is in the **expected format**
- Values are within **acceptable range**
* This is important because C **does not automatically validate input**, so the programmer must handle it manually.
## Types of Data Checking
### 1. Range Checking
Ensures the value lies within a specific range.
#### Example
```c
int age;
scanf("%d", &age);
if (age >= 0 && age <= 120) {
    printf("Valid age");
} else {
    printf("Invalid age");
}
```
## 2. Type Checking (Basic Validation)
Ensures correct data type is entered.
- Note: `scanf()` does not fully protect against wrong input (like entering a character instead of an integer).
### Safer Approach
```c
int num;
if (scanf("%d", &num) != 1) {
    printf("Invalid input");
}
```
## 3. Logical Checking
Checks whether data makes logical sense.
### Example
```c
int start = 10, end = 5;
if (start < end) {
    printf("Valid range");
} else {
    printf("Invalid range");
}
```
## 4. Format Checking
Ensures input follows a specific format (like email, phone number).
### Example (Basic)
```c
char ch;
scanf(" %c", &ch);
if (ch >= 'A' && ch <= 'Z') {
    printf("Uppercase letter");
}
```
## 5. Re-prompting User (Validation Loop)
Keeps asking until valid input is given.
### Example
```c
int num;
while (1) {
    printf("Enter a positive number: ");
    scanf("%d", &num);
    if (num > 0)
        break;
    printf("Invalid input. Try again.\n");
}
```
## Why Data Checking is Important?
- Prevents **runtime errors**
- Avoids **unexpected behavior**
- Improves **program reliability**
- Enhances **user experience**
- Protects against **invalid or malicious input**
## Real-Time Example
```c
int marks;
do {
    printf("Enter marks (0-100): ");
    scanf("%d", &marks);
} while (marks < 0 || marks > 100);
printf("Valid marks entered: %d", marks);
```
