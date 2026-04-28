## Fundamentals of ARM
### 1. What is ARM?
**ARM (Advanced RISC Machine)** is a family of **32-bit (and now also 64-bit) RISC architectures** developed by Arm Holdings.
It is widely used in **embedded systems** due to its **low power consumption, high performance, and small size**.
## 2. Key Characteristics of ARM
- **RISC Architecture**
  - Simple instructions
  - Fixed instruction size (mostly 32-bit)
- **Load/Store Architecture**
  - Data is processed in registers only
- **Large Register Set**
  - Reduces memory access
- **Low Power Consumption**
  - Ideal for mobile & embedded devices
- **High Performance**
  - Efficient pipeline execution
## 3. ARM Processor Features
- **Pipelining**
  - Execution divided into stages (Fetch → Decode → Execute)
- **Conditional Execution**
  - Almost every instruction can be conditionally executed
- **Multiple Operating Modes**
  - User, FIQ, IRQ, Supervisor, etc.
- **Interrupt Handling**
  - Fast response to external/internal events
- **Thumb Mode**
  - 16-bit instructions for better code density
## 4. ARM Register Set
ARM has **16 general-purpose registers:**
| Register | Name                 | Function                       |
| -------- | -------------------- | ------------------------------ |
| R0–R12   | General Purpose      | Data storage                   |
| R13      | SP (Stack Pointer)   | Points to stack                |
| R14      | LR (Link Register)   | Stores return address          |
| R15      | PC (Program Counter) | Holds next instruction address |
Special register:
- **CPSR (Current Program Status Register)**
  - Stores flags (Zero, Carry, Negative, Overflow)
  - Controls processor state
## 5. ARM Instruction Set Basics
- **Data Processing**
  - ADD, SUB, MOV, CMP
- **Memory Access**
  - LDR (Load), STR (Store)
- **Branching**
  - B, BL (Branch with Link)
- **Shift Operations**
  - Logical and arithmetic shifts
### Example:
```assembly
MOV R0, #5
ADD R1, R0, #3
```
## 6. ARM Pipeline Concept
Typical ARM pipeline has **3 stages**:
1. Fetch – instruction fetched from memory
2. Decode – instruction decoded
3. Execute – operation performed
- Advantage: **Increases speed by overlapping instructions**
## 7. ARM Operating Modes
- **User Mode** – Normal program execution
- **FIQ Mode** – Fast interrupt handling
- **IRQ Mode** – Standard interrupt
- **Supervisor Mode** – OS/kernel operations
## 8. ARM Applications
ARM processors are used in:
- Smartphones & tablets
- Embedded systems
- IoT devices
- Consumer electronics
- Networking devices
## 9. Advantages of ARM
- Power efficient
- Cost-effective
- High code density
- Scalable architecture
## 10. Summary
ARM is a **powerful, efficient, and widely used RISC architecture** designed for modern embedded systems. Its **simple instruction set, pipelining, and low power usage** make it dominant in mobile and embedded applications.
