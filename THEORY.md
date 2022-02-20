# GCSE Computer Science: theory working document

## 1.1 Systems architecture

### 1.1.1 The purpose of the CPU[^1]

The CPU *(Central Processing Unit)* is often referred to as the hypothetical 'brain' of the computer. It has two main functions:
 - To process data and instructions
 - To control and manage the overall computer system

*Most* processing is run in the CPU ('most' because more graphical programs often make use of the GPU, such as with OpenGL).

### 1.1.2 The von Neumann architecture[^1]

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

###### Jack Bennett

[^1]: https://www.bbc.co.uk/bitesize/guides/zbfny4j
