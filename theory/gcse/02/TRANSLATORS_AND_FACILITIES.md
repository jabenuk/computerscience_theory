# 2.5 Translators and facilities of languages

## 2.5.1 Characteristics and purposes of different levels of programming language

**Source code** refers to any code written in a [high-level programming language](#high-level-languages).

### High level languages

Since machine code is a pain to work with, the majority of developers work with **high level programming languages.**

These languages aim to be similar to the written and spoken language of the developer *(assuming they speak English, in most cases)*. Keywords such as `if`, `switch`, `case`, `do`, and `return` mimic their equivalents in the English language. For example- in C, the function `printf()` stands for '**print f**ormatted text'.

One disadvantage of high-level programming languages is that the developer sometimes has no idea how a lot of the built-in functions work, limiting their knowledge of the language. However, a major advantage is that they allow developers to focus on what needs to be done instead of worrying about more problems that low-level languages could cause.

Some extremely high-level programming languages are **Python** and **JavaScript**. Some lower-level languages could be **C#** and **Java**. Languages that are even further low-level are **C** and **C++**.

### Low level languages

**Low level languages** are languages that sit close to the processor's instruction set (the set of instructions the CPU can carry out).

#### Machine code

Machine code is the the exact instructions that a processor understands and can act upon.

The primary advantage of machine code is that it gives the programmer **ultimate control** over the processor, allowing for **extreme optimisations** and things that may be **impossible in high-level languages.**

However, machine code is also **notoriously hard to write in and understand** - to the point where the advantages are completely outweighed by the sheer impracticality of manually writing machine code.

#### Assembly language

Assembly sits between machine code and high-level programming languages. Here are some examples of Assembly mnemonics (short abbreviations):

| Mnemonic | Action |
| - | - |
| `lda` | Load a value from an address. |
| `sta` | Store a value in an address. |
| `add` | Add the value held in an address to the value held in the accumulator. |
| `sub` | Subtract from the accumulator the value held in an address. |
| `mov` | Move the contents of one address to another. |

Assembly can sometimes be practical; it gives as much control as raw machine code with a lot more readability.

## 2.5.2 A comparison between translators

A **translator** is any program that converts source code into object code, a form that computers understand.

### Compilers

A **compiler** takes all source code and translates into object code all in one go (**compilation**). The object code can then be run at any time.

Compilers have advantages:
 - compiled programs run quickly; they have already been translated
 - compiled programs can be supplied as an **executable**
 - compilers optimise code, allowing code to run quicker and take up less memory space

And disadvantages:
 - there must be enough memory space to hold the source code, compiler, and the generated object code - in addition to temporary working space for the compiler to perform the translation. This isn't a problem for modern systems
 - a lot of errors will likely have to be detected at runtime
 - source code compiled on one platform will not run on another - object code is specific to the processor's architecture

### Interpreters

For some reason, some people like **interpreters.** An interpreter translates source code to object code one instruction at a time, executing the code immediately - this is **interpretation.**

Interpreters have advantages:
 - instructions are executed as soon as they are translated
 - since instructions are executed once translated, they are not stored for later use. As a result, interpreters require less available memory
 - once an error is found, the program stops running and the user is notified where the error came from in the code, helping with debugging
 - interpreted code is cross-platform

And disadvantages:
 - interpreted programs run far slower as the processor has to wait for each instruction to be processed
 - the program has to be translated every time it is run
 - no executable file is produced, so the source code has to be supplied
 - interpreters do **not** optimise code

### Assemblers

**Assemblers** translate assembly code into object code. One machine code instruction is generated for each assembly instruction.

## 2.5.3 Common tools and facilities available in an IDE

There are a lot of tools that exist to make developers' lives easier. Here are some:
 - text editors
 - error trapping
 - breakpoints
 - automatic line numbering
 - syntax highlighting
 - variable tracing
 - automatic indentation
 - suggestions (e.g. Intellisense)

Some or all of these tools can be bundled together into one single **integrated development environment**. Here are some examples of IDEs:
 - **Visual Studio**, built for C# but also works reasonably well for languages such as C/C++
 - **Eclipse** and **Netbeans** are good for Java development
 - **JetBrains** offers a variety of proprietary IDEs for C#, Java, Python, etc.
 - **Python IDLE** wrongly calls itself an "IDE"

### Editors

Editors offer facilities such as line numbers, syntax highlighting, and intelligent code completion.

### Error diagnostics

Most IDEs have debugging tools of some sort, like **breakpoints** (pausing the program at predetermined points), **variable tracing** (trace/watch the changing values stored in variables), and **error trapping** (pinpoint exactly where an exception is encountered or where a syntax error occured).

### Runtime environment (RTE)

An RTE allows programs to run on a computer, even if they aren't designed for that computer's architecture, by creating a virtual machine to run the program through. One example of an RTE is the **Java Runtime Environment (JRE)**, which runs Java byte-code through the **Java Virtual Machine (JVM)**.

## References

### Sections
 - [2.5.1 Characteristics and purposes of different levels of programming language](https://www.bbc.co.uk/bitesize/guides/z6x26yc/revision/1)
 - [2.5.2 A comparison between translators](https://www.bbc.co.uk/bitesize/guides/z6x26yc/revision/5)
 - [2.5.3 Common tools and facilities available in an IDE](https://www.bbc.co.uk/bitesize/guides/z6x26yc/revision/6)
