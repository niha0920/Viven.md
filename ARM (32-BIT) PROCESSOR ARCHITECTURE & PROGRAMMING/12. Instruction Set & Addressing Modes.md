## Instruction Set & Addressing Modes (ARM Architecture)
### 1. Instruction Set (ARM)
The **instruction set** is the collection of operations that a processor can execute. In ARM (a Reduced Instruction Set Computing architecture), instructions are designed to be:
- Simple and fixed-length (mostly 32-bit)
- Executed in a single cycle (ideal case)
- Efficient for pipelining
#### Types of ARM Instructions
##### 1. Data Processing Instructions
Used for arithmetic and logical operations.
- Examples: `ADD`, `SUB`, `AND`, `ORR`, `MOV`, `CMP`
- Work only on registers (no direct memory access)
###### Example:
```asm
ADD R0, R1, R2   ; R0 = R1 + R2
```
## 2. Data Transfer Instructions
Used to move data between memory and registers.
- `LDR` (Load Register)
- `STR` (Store Register)
### Example:
```asm
LDR R0, [R1]     ; Load value from memory address in R1 into R0
STR R0, [R1]     ; Store value of R0 into memory
```
## 3. Branch Instructions
Used for program control flow.
- `B` (Branch)
- `BL` (Branch with Link – function call)
- `BX` (Branch and exchange instruction set)
### Example:
```asm
B LOOP
```
## 4. Multiply Instructions
- `MUL`, `MLA`
### Example:
```asm
MUL R0, R1, R2   ; R0 = R1 × R2
```
## 5. Status Register Instructions
Used to update or read flags in CPSR (Current Program Status Register).
## 2. Addressing Modes
**Addressing modes** define how operands (data) are accessed.
## Types of Addressing Modes in ARM
### 1. Immediate Addressing Mode
Operand is directly given in the instruction.
#### Example:
```asm
MOV R0, #10   ; Load constant 10 into R0
```
## 2. Register Addressing Mode
Operand is in a register.
### Example:
```asm
ADD R0, R1, R2
```
## 3. Register Indirect Addressing
Register contains the memory address.
### Example:
```asm
LDR R0, [R1]
```
## 4. Indexed Addressing Mode (Offset)
Address is computed using base register + offset.
### Example:
```asm
LDR R0, [R1, #4]
```
## 5. Pre-indexed Addressing
Address is updated before accessing memory.
### Example:
```asm
LDR R0, [R1, #4]!
```
## 6. Post-indexed Addressing
Address is updated after accessing memory.
### Example:
```asm
LDR R0, [R1], #4
```
## 7. PC-relative Addressing
Uses the Program Counter (PC) to access memory (useful for jumps, constants).
### Example:
```asm
LDR R0, [PC, #offset]
```
## Key Difference
| Feature | Instruction Set    | Addressing Modes             |
| ------- | ------------------ | ---------------------------- |
| Purpose | Defines operations | Defines how data is accessed |
| Example | `ADD`, `SUB`       | Immediate, Register, Indexed |
| Role    | Execution          | Operand access               |
## Quick Summary
- **Instruction Set** = What operation to perform
- **Addressing Mode** = Where to get the data from
