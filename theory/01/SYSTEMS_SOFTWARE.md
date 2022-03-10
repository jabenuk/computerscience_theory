# 1.7 Systems software

Systems software is any software that governs the computer system. It:
 - controls the hardware
 - allows other programs to run
 - provides an interface for the user to interact with the computer
 - maintains the system

## 1.7.1 Features of an operating system

### User interface

 - **GUI**: Graphical User Interface
 - **Mobile UI**
 - **CLI**: Command Line Interface

### Memory management

Memory should be managed so that multiple programs can run simultaneously. One method of memory management is **paging**, where memory is broken up into fixed-size blocks known as **pages.** Different OSs allocate different page sizes. Memory pages in modern operating systems are typically **4 KB** in size.

The OS determines how much memory programs require on execution, and allocates enough pages to hold the program and its data. When the program is closed, the allocated memory is freed up for use by other programs.

The pages a program occupies **may or may not be contiguous** *(one after the other)* but this does not matter. The OS knows what pages to fetch data from.

### Multitasking

To multitask is to run more than one program simultaneously. CLIs usually multitask by using multiple shells, but GUIs have *'windows'* instead.

Multitasking is possible if:
 - the OS supports multitasking
 - there is enough memory available to hold multiple programs

### Peripheral management and drivers

To operate peripherals, operating systems make use of **device drivers** - these contain instructions on how to control a device (e.g. peripheral). Each connected device has its own driver. Advantages of drivers include:
 - any device can be used with any operating system, as long as there is an available driver for it
 - they can be updated, usually to be optimised or fix bugs

### User management

Operating systems manage users. They allow:
 - individual users to be created and deleted
 - access levels to differ between users (such as **sudo/administrator rights**)
 - the auditing of files a user creates, accesses, edits, and deletes

### File management

File handling and maintenance is one of the most important tasks of an OS. The file manager allows users to:
 - create, modify, and delete files and directories
 - copy and duplicate files and directories
 - move files and directories
 - rename files and directories
 - sort items into different orders such as by name, file type, date created, etc
 - search for particular files or directories
 - restore deleted files
 - permissions to be set on particular files (e.g. read-only or edit)

## References

### Sections

 - [1.7.1 Features of an operating system](https://www.bbc.co.uk/bitesize/guides/zmqw7p3/revision/2)
