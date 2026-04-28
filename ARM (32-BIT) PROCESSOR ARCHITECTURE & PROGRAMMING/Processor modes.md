In ARM architecture, **processor modes** define the operating state of the CPU. Each mode determines **privilege level, accessible resources, and purpose** (user program, OS, interrupt handling, etc.).
## ARM Processor Modes
ARM processors (like ARM7/ARM9) have **7 main modes**:
### 1. User Mode (USR)
- **Normal program execution mode**
- Unprivileged (cannot access system control registers)
- Used for application programs
## 2. System Mode (SYS)
- Privileged version of User mode
- Same registers as User mode
- Used by OS for running privileged tasks
## 3. Supervisor Mode (SVC)
- Entered after **reset** or software interrupt (SWI)
- Privileged mode
- Used by operating systems for **system calls**
## 4. Abort Mode (ABT)
- Activated on **memory access failure**
- Helps in handling memory faults (like invalid address access)
## 5. Undefined Mode (UND)
- Entered when CPU encounters **undefined instruction**
- Used for emulation or debugging
## 6. Interrupt Mode (IRQ)
- Handles **normal interrupts**
- Lower priority interrupt handling
## 7. Fast Interrupt Mode (FIQ)
- Handles **high-priority interrupts**
- Faster than IRQ (more registers available → less overhead)
## Summary Table
| Mode             | Type         | Purpose                        |
| ---------------- | ------------ | ------------------------------ |
| User (USR)       | Unprivileged | Normal program execution       |
| System (SYS)     | Privileged   | OS-level tasks                 |
| Supervisor (SVC) | Privileged   | OS, reset, system calls        |
| Abort (ABT)      | Privileged   | Memory fault handling          |
| Undefined (UND)  | Privileged   | Undefined instruction handling |
| IRQ              | Privileged   | Normal interrupt handling      |
| FIQ              | Privileged   | Fast interrupt handling        |
## Key Concept
- ARM modes are divided into:
### Unprivileged Mode
- User (USR)
### Privileged Modes
- SYS, SVC, ABT, UND, IRQ, FIQ
## Important Features
- Each mode has its **own banked registers** (especially FIQ for speed)
- Switching modes happens automatically on:
  - Interrupts
  - Exceptions
  - Software instructions
- Ensures **security, stability, and efficient interrupt handling**
## Quick Memory Trick
"**US SAUIF**"
- U → User
- S → System
- S → Supervisor
- A → Abort
- U → Undefined
- I → IRQ
- F → FIQ
