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
