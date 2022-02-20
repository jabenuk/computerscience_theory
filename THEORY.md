# GCSE Computer Science: theory working document

## 1.1 Systems architecture

### 1.1.1 The purpose of the CPU ([^1])

The CPU *(Central Processing Unit)* is often referred to as the hypothetical 'brain' of the computer. It has two main functions:
 - To process data and instructions
 - To control and manage the overall computer system

*Most* processing is run in the CPU ('most' because more graphical programs often make use of the GPU, such as with OpenGL).

### 1.1.2 The von Neumann architecture ([^1])

The 'von Neumann archictecture' refers to the design/specification set out by John von Neumann, and is in use in most modern general-purpose computers. The key elements of the von Neumann architecture are laid out as the following:
 - both data and instructions are stored in binary format.
 - data and instructions are both stored in primary memory.
 - instructions are fetched from memory *one at a time* and *in sequence*.
 - the CPU **decodes** and **executes** an instruction before cycling around to **fetch** the next instruction.
 - this cycle continues until no more instructions are available.

A CPU based on the von Neumann architecture has five key registers *(high-speed memory caches)* that are used for processing:
 - the **program counter (PC)** holds the memory address of the *next* instruction to be fetched.
 - the **memory address register (MAR)** holds either:
    - the address of the current instruction to be fetched from memory
    - the address in memory to which data is to be transferred
 - the **memory data register (MDR)** holds either:
    - the data found at the address in the MAR
    - the data which is to be transferred to primary memory
 - the **current instruction register (CIR)** holds the instruction currently being decoded + executed
 - finally, the **accumulator (ACC)** temporarily holds the data being processed and the results of processing

### 1.1.3 The von Neumann 'fetch-decode-execute' cycle ([^1])

The fetch-decode-execute cycle is strictly followed by von Neumann CPUs to process each instruction. The cycle is most commonly described as:
 1. the memory address held in the *program counter (PC)* is copied into the *memory address register (MAR)*.
 2. the address in the program counter is then incremented by one so it, again, holds a pointer to the next instruction.
 3. the CPU gets the data/instruction held in the MAR via the *address bus* - this information is copied into the *memory data register (MDR)*.
 4. the instruction/data in the MDR is then copied into the *current instruction register (CIR)*.
 5. the instruction/data in the CIR is **decoded** and finally **executed**. The results of this processing are stored in the *accumulator (ACC)*.
 6. the cycle returns to step 1.

Depending on the type of instruction, additional steps may be taken:
 - if the instruction is to transfer data from the ACC *back to* primary memory:
    1. the intended memory address is copied into the MAR.
    2. the data to be transferred is copied into the MDR.
    3. the data is then transferred to the specified address using the *address bus* and *data bus*.
 - the executed instruction may require the program to 'jump' to a different place in the program *(e.g. function or goto calls)*. In this case:
    1. the memory address of the *new* next instruction to be fetched is copied into the program counter (PC).
    2. the process then **immediately breaks and returns to step 1**, continuing the cycle for wherever the program 'jumped' to.

It can be simplified and summarised with a diagram such as this one:

<img src="/resources/fetch-decode-execute.png" height=150px/>

###### Jack Bennett

[^1]: https://www.bbc.co.uk/bitesize/guides/zbfny4j
