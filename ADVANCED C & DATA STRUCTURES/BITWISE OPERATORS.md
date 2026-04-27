# AND (&), OR (|), XOR (^)
These are **bitwise operators in C**, used to perform operations at the **binary (bit) level** of integers.
## 1. Bitwise AND `&`
### Definition
The AND operator compares each bit of two numbers:
- Result bit = **1 only if both bits are 1**
- Otherwise, result = 0
## Truth Table
| A | B | A & B |
| - | - | ----- |
| 0 | 0 | 0     |
| 0 | 1 | 0     |
| 1 | 0 | 0     |
| 1 | 1 | 1     |
### Example
```c
int a = 5;   // 0101
int b = 3;   // 0011
int c = a & b; // 0001 → 1
```
#### Used for:
- Masking bits
- Checking specific bits
## 2. Bitwise OR `|`
### Definition
The OR operator compares each bit:
- Result bit = **1 if at least one bit is 1**
### Truth Table
| A | B | A \| B |
|---|---|------ |
| 0 | 0 | 0     |
| 0 | 1 | 1     |
| 1 | 0 | 1     |
| 1 | 1 | 1     |
### Example
```c
int a = 5;   // 0101
int b = 3;   // 0011
int c = a | b; // 0111 → 7
```
#### Used for:
- Setting bits
- Combining flags
## 3. Bitwise XOR `^`
### Definition
The XOR (exclusive OR) compares each bit:
- Result bit = **1 if bits are different**
- Result = 0 if bits are same
### Truth Table
| A | B | A ^ B |
| - | - | ----- |
| 0 | 0 | 0     |
| 0 | 1 | 1     |
| 1 | 0 | 1     |
| 1 | 1 | 0     |
### Example
```c
int a = 5;   // 0101
int b = 3;   // 0011
int c = a ^ b; // 0110 → 6
```
#### Used for:
- Toggling bits
- Swapping values (without temp variable)
## Quick Comparison
| Operator | Symbol | Rule                 | Example Result |
| -------- | ------ | -------------------- | -------------- |
| AND      | `&`    | 1 if both bits are 1 | 5 & 3 = 1      |
| OR       | `\|`   | 1 if any bit is 1    | 5 | 3 = 7      |
| XOR      | `^`    | 1 if bits differ     | 5 ^ 3 = 6      |
## Key Insight
- `&` → **Check / mask**
- `|` → **Set bits**
- `^` → **Toggle bits**

# Compliment (~)
## Bitwise Complement `~` (NOT operator)
### Definition
The **bitwise complement (`~`)** flips every bit of a number:
- `1 → 0`
- `0 → 1`
## How it Works
It performs **1’s complement** on the binary representation.
### Example
```c
int a = 5;      // Binary: 0000 0101
int b = ~a;     //        1111 1010
```
Now, in most systems (using **2’s complement representation**):
```
~5 = -6
```
## Why does `~5 = -6`?
Steps:
1. Binary of 5 → `0000 0101`
2. Apply `~` → `1111 1010`
3. This represents a negative number in 2’s complement
4. Convert to decimal → **-6**
- Shortcut formula:
```
~x = -(x + 1)
```
## More Examples
```c
~0  = -1
~1  = -2
~10 = -11
```
## Uses
-  Flipping bits
- Creating masks
- Low-level programming (embedded systems, drivers)
## Quick Summary
| Operator   | Symbol | Operation        |
| ---------- | ------ | ---------------- |
| Complement | `~`    | Inverts all bits |
| Formula    | —      | `~x = -(x + 1)`  |
## Key Insight:
Unlike `&`, `|`, `^`, this is a **unary operator** (works on only one operand).

# Left-shift (<<), Right-shift (>>)
## 1. Left Shift `<<`
### Definition
The **left shift operator (`<<`)** shifts all bits of a number to the **left** by a given number of positions.
- Zeros are filled on the right side
- Leftmost bits are discarded
## Example
```c
int a = 5;      // 0000 0101
int b = a << 1; // 0000 1010 → 10
```
```c
int c = a << 2; // 0001 0100 → 20
```
## Key Idea
###
Each left shift by 1 ≈ **multiply by 2**
- `x << 1 = x × 2`
- `x << n = x × (2ⁿ)`
## Uses
- Fast multiplication
- Bit manipulation
- Setting bit positions
## 2. Right Shift `>>`
### Definition
The **right shift operator (`>>`)** shifts bits to the **right**.
- Rightmost bits are discarded
- Left side filling depends on the type:
  - **Unsigned** → filled with 0
  - **Signed** → usually fills with sign bit (implementation-dependent)
## Example
```c
int a = 20;     // 0001 0100
int b = a >> 1; // 0000 1010 → 10
```
```c
int c = a >> 2; // 0000 0101 → 5
```
## Key Idea
###
Each right shift by 1 ≈ **divide by 2**
- `x >> 1 = x / 2`
- `x >> n = x / (2ⁿ)`
###
For signed numbers, behavior may vary slightly
## Important Note (VERY IMPORTANT)
- Left shift overflow → **undefined behavior in C**
- Right shift of negative numbers → **implementation-dependent**
## Quick Comparison
| Operator | Direction | Effect        |
| -------- | --------- | ------------- |
| `<<`     | Left      | Multiply by 2 |
| `>>`     | Right     | Divide by 2   |
## Key Insight
- `<<` → moves bits **towards higher value**
- `>>` → moves bits **towards lower value**

# Masking, Setting and Testing of Bit/Bits
## Bit Manipulation: Masking, Setting, and Testing Bits
These are **very important concepts in C**, especially for **embedded systems, drivers, and interviews**.
## 1. Masking (Clearing bits)
### Definition
**Masking** is used to **clear (set to 0) specific bits** using the **AND (`&`) operator**.
## How it Works
- Use a mask with **0s where bits should be cleared**
- Use **1s where bits should remain unchanged**
## Example
```c
int a = 13;        // 1101
int mask = 10;     // 1010
int result = a & mask; // 1000 → 8
```
## Clear a specific bit
```
a = a & ~(1 << 2);   // Clears 2nd bit
```
- `~(1 << 2)` → creates mask with 0 at position 2
## 2. Setting Bits
### Definition
**Setting a bit** means making it **1**, using the **OR (`|`) operator**.
## How it Works
- Use a mask with **1 at positions you want to set**
## Example
```c
int a = 8;         // 1000
int result = a | 4; // 1100 → 12
```
## Set a specific bit
```c
a = a | (1 << 1);   // Sets 1st bit
```
- Even if bit is already 1, it remains 1
## 3. Testing Bits
### Definition
**Testing a bit** means checking whether a bit is **0 or 1**.
## How it Works
- Use **AND (`&`)** with a mask
- If result ≠ 0 → bit is **1**
- If result = 0 → bit is **0**
## Example
```c
int a = 10; // 1010
if (a & (1 << 3)) {
    printf("Bit is set");
} else {
    printf("Bit is not set");
}
```
## Combined Example
```c
int a = 5;   // 0101
// Set 1st bit
a = a | (1 << 1);   // 0111
// Clear 2nd bit
a = a & ~(1 << 2);  // 0011
// Test 0th bit
if (a & (1 << 0))
    printf("Bit 0 is ON");
```
## Quick Summary
| Operation | Operator | Purpose    |          
| --------- | -------- | ---------- | 
| Masking   | `&`      | Clear bits |          
| Setting   | `\| `    | Set bits   |
| Testing   | `&`      | Check bits |          
## Key Insight (Very Important)
- `1 << n` → creates a mask for **nth bit**
- Combine with:
  - `&` → clear/test
  - `|` → set
