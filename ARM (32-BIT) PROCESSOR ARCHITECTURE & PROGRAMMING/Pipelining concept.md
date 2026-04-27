## Pipelining Concept (Computer Architecture)
Pipelining is a technique used in processors (especially in RISC architectures like ARM Holdings designs) to **increase instruction execution speed** by overlapping multiple instructions.
## Basic Idea
Instead of executing one instruction completely before starting the next, pipelining **breaks execution into stages** and processes multiple instructions simultaneously—just like an assembly line.
## Everyday Analogy 🍔
Think of making burgers in a fast-food shop:
1. One person takes orders
2. Another prepares ingredients
3. Another cooks
4. Another packs
* Each person works in parallel → **more burgers per minute**
* Same idea in CPUs → **more instructions per unit time**
## Typical Pipeline Stages (5-stage pipeline)
<img width="600" height="367" alt="image" src="https://github.com/user-attachments/assets/5e087a46-a2e5-41d5-b083-746ad34b98a2" />

1. **IF (Instruction Fetch)**
* Fetch instruction from memory
2. **ID (Instruction Decode)**
* Decode instruction & identify operands
3. **EX (Execute)**
* Perform operation (ALU, calculations)
4. **MEM (Memory Access)**
* Read/write data from/to memory
5. **WB (Write Back)**
* Store result in register
## How It Works
Without pipelining:
```
Instruction 1 → completes → Instruction 2 → starts
```
With pipelining:
```
Cycle 1: IF (I1)
Cycle 2: ID (I1) + IF (I2)
Cycle 3: EX (I1) + ID (I2) + IF (I3)
...
```
- Multiple instructions are in different stages at the same time.
## Key Advantage
- **Increases throughput** (more instructions completed per second)
- Better CPU utilization
- Ideal for RISC processors like ARM
### Important:
It does **NOT reduce execution time of a single instruction**, but increases overall performance.
## Pipeline Hazards (Problems)
1. **Data Hazard**
* When one instruction depends on result of another
2. **Control Hazard**
* Due to branch/jump instructions
3. **Structural Hazard**
* Hardware resource conflicts
## Simple Example
```
Instruction 1: ADD R1, R2, R3
Instruction 2: SUB R4, R1, R5
```
Here, Instruction 2 depends on Instruction 1 → causes **data hazard**
## Pipelining in ARM
- Classic ARM (like ARM7) uses a **3-stage pipeline**
  - Fetch → Decode → Execute
- Advanced ARM processors use **5+ stages**
## Final Summary
Pipelining is like:
- **Assembly line in hardware**
- Executes multiple instructions in parallel (different stages)
- Improves performance without increasing clock speed
