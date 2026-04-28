The **ARM Programming Model** defines how a programmer interacts with the ARM processor using its **instruction set** and **assembly language**. It describes registers, instruction formats, and how programs are written and executed.
## 1. ARM Instruction Set
The **ARM Instruction Set** is based on **RISC (Reduced Instruction Set Computer)** principles:
### Key Features
- **Fixed instruction length**: 32-bit (in ARM mode)
- **Load/Store architecture**: Memory accessed only via load/store instructions
- **Large register set**: 16 general-purpose registers
- **Conditional execution**: Almost every instruction can be conditionally executed
- **Pipelining support**: Improves performance
## Types of ARM Instructions
### 1. Data Processing Instructions
Used for arithmetic and logical operations.
#### Examples:
- `ADD R1, R2, R3` → R1 = R2 + R3
- `SUB R1, R2, #5`
- `AND`, `ORR`, `EOR`, `MOV`, `CMP`

##### Operate only on registers (not directly on memory)
## 2. Load/Store Instructions
Used to transfer data between memory and registers.
### Examples:
- `LDR R1, [R2]` → Load from memory
- `STR R1, [R2]` → Store to memory
#### ARM does NOT allow direct memory-to-memory operations.
## 3. Branch Instructions
Used for program control (loops, jumps).
### Examples:
- `B LABEL` → Unconditional branch
- `BL FUNCTION` → Branch with link (used for function calls)
- `BX LR` → Return from function
## 4. Multiply Instructions
- `MUL R1, R2, R3`
- `MLA R1, R2, R3, R4`
## 5. Software Interrupt
- `SWI` → Used for system calls
## Conditional Execution
Each instruction can have a condition suffix:
### Examples:
- `ADDEQ R1, R2, R3` → Execute if equal
- `SUBNE R1, R2, R3` → Execute if not equal
#### Based on CPSR flags (Zero, Carry, Negative, Overflow)
## 2. ARM Registers (Programming Model)
<img width="1024" height="768" alt="image" src="https://github.com/user-attachments/assets/eb3d6f98-4d5e-43fa-800c-9c3792c5906e" />
<img width="2048" height="1448" alt="image" src="https://github.com/user-attachments/assets/f237fa6c-5fbe-4285-9f67-d3e2ef831be9" />

### General Purpose Registers
- **R0 – R12** → General use
### Special Registers
- **R13 (SP)** → Stack Pointer
- **R14 (LR)** → Link Register (return address)
- **R15 (PC)** → Program Counter
### Status Register
- **CPSR (Current Program Status Register)**
  - N → Negative
  - Z → Zero
  - C → Carry
  - V → Overflow
## 3. ARM Assembly Language Programming
Assembly language is a **low-level programming language** used to write programs directly for ARM processors.
## Basic Syntax
```assembly
LABEL   INSTRUCTION   OPERANDS   ; COMMENT
```
Example:
```assembly
MOV R0, #10      ; Load 10 into R0
ADD R1, R0, #5   ; R1 = R0 + 5
```
## Example Program (Addition)
```assembly
AREA PROGRAM, CODE, READONLY
ENTRY
MOV R0, #5       ; First number
MOV R1, #7       ; Second number
ADD R2, R0, R1   ; R2 = R0 + R1
END
```
## Example: Loop
```assembly
MOV R0, #5       ; Counter
LOOP
SUB R0, R0, #1
CMP R0, #0
BNE LOOP         ; Repeat until zero
```
## Example: Function Call
```assembly
BL FUNCTION      ; Call function
FUNCTION
ADD R0, R0, #1
BX LR            ; Return
```
## 4. Addressing Modes in ARM
### Common Addressing Modes:
#### 1. Immediate
```
MOV R0, #10
```
#### 2. Register
```
MOV R1, R2
```
#### 3. Register Indirect
```
LDR R0, [R1]
```
#### 4. Indexed
```
LDR R0, [R1, #4]
```
#### 5. Pre/Post Indexed
```
LDR R0, [R1, #4]!
LDR R0, [R1], #4
```
## 5. Key Advantages of ARM Programming Model
- Simple and efficient instruction set
- High performance due to pipelining
- Low power consumption
- Flexible conditional execution
- Widely used in embedded systems
## Summary
The **ARM Programming Model** includes:
- **Instruction Set** → Defines operations (ADD, LDR, B, etc.)
- **Registers** → R0–R15 + CPSR
- **Assembly Language** → Low-level programming using ARM instructions
- **Addressing Modes** → Ways to access data
