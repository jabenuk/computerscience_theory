# 1.2 Memory

## 1.2.1 Primary storage, also known as memory

Primary memory is built inside the computer; therefore, data can be read from and written to it very quickly. There are two types of primary memory:
 - **read-only memory (ROM)** is *non-volatile*.
 - **random access memory (RAM)** is *volatile*.

## 1.2.2 Read-only memory (ROM)

Read-only memory is non-volatile; **contents are not lost when the computer is turned off.**

ROM is ususally used for instructions on how the computer should boot. One example of a program stored in the ROM is the **BIOS** (*B*asic *I*nput/*O*utput *S*ystem) - the BIOS is started when the computer is turned on, and - after checking for hardware errors - runs a **bootloader** (like GRUB or the proprietary Windows Boot Manager) that then boots into the desired operating system. In this case, the operating system is loaded from the secondary storage to the RAM.

## 1.2.3 Random access memory (RAM)

Random access memory is volatile memory; **once the computer is turned off, data stored in RAM is lost.** Note that the 'random access' part stems from the fact that data can be stored and accessed from *any location* within the memory.

RAM holds any running programs and services, including the operating system, desktop environment, window manager, etc.

Being read/write, the contents of RAM can be changed at any time by the program that initially allocated the memory. RAM can be **easily upgraded**, unlike other forms of memory.

## 1.2.4 Virtual memory

Virtual memory is the use of secondary storage as memory. It is used when the amount of RAM needed is greater than the amount of RAM available to the computer.

It allows data in [RAM](#123-random-access-memory-ram) that is **not currently being used** to be transferred to the secondary storage. This frees up room in the RAM for programs and data that **are** being used. When the data on the hard disk is needed again, it is **swapped** with any other unused data in the RAM (that is to say, it is transferred back to the RAM and some other unused data is transferred to virtual memory).

Sidenote: normally, the operating system allocates space on the secondary storage device for virtual memory. In Linux, for example, this is appropriately referred to as **swap space,** and is often partitioned by the user during installation.

Virtual memory is a **lot** slower than RAM, as secondary storage devices have slower access speeds than memory. Plus, the CPU has to wait whilst data is swapped between RAM and swap space. This is why upgrading the RAM in a computer can greatly increase performance; virtual memory is no longer needed.

## 1.2.5 Cache memory

Cache memory is [RAM](#123-random-access-memory-ram) that is **built into the CPU.**

Data can be transferred to and from cache memory more quickly than RAM. Because of this, cache memory is used to temporarily hold data and instructions that the CPU is **likely to reuse,** so it doesn't have to wait for the information to be fetched from RAM. Of course, the more cache there is, the faster the computer runs - however, it is expense to build due to its high-speed performance so tends to be very small in size.

To get around this issue, different levels of cache exist:
 - **L1 cache**: extremely fast transfer rates, but very small in size. Holds most frequently used information.
 - **L2 cache**: larger in capacity than L1, but slower in speed. Holds information used less frequently.

## 1.2.6 Flash memory

Flash memory is a **non-volatile form of [RAM](#123-random-access-memory-ram).** It requires little power and contains no moving parts, so it is an ideal storage medium for devices such as tablets, smartphones, and digital cameras. It is not as fast as RAM, however.

Flash memory is also often used as **external secondary storage**, such as in USB sticks and SSDs.

## References

### Sections
 - [1.2.1 Primary storage, also known as memory](https://www.bbc.co.uk/bitesize/guides/zd4r97h/revision/1)
 - [1.2.2 Read-only memory (ROM)](https://www.bbc.co.uk/bitesize/guides/zd4r97h/revision/2)
 - [1.2.3 Random access memory (RAM)](https://www.bbc.co.uk/bitesize/guides/zd4r97h/revision/3)
 - [1.2.4 Virtual memory](https://www.bbc.co.uk/bitesize/guides/zd4r97h/revision/4)
 - [1.2.5 Cache memory](https://www.bbc.co.uk/bitesize/guides/zd4r97h/revision/5)
 - [1.2.6 Flash memory](https://www.bbc.co.uk/bitesize/guides/zd4r97h/revision/6)
