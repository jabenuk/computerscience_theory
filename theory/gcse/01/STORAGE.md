# 1.3 Storage

## 1.3.1 Secondary storage, also known as storage

Secondary storage refers to any **non-volatile**, **long-term** storage media; it is necessary to keep programs and data indefinitely (or in the case of hard drives, until they inevitable fail). Without it, all data would be lost as soon as the computer is turned off (see [memory](/theory/01/MEMORY.md)).

Not all computers need secondary storage - for example, embedded computers store any user data in **RAM** and any built-in instructions in **ROM**.

## 1.3.2 Data capacity

The conventional data units can be seen below.

| Unit | Amount of bytes |
| ---- | --------------- |
| Byte (B) | 1 |
| Kilobyte (KB) | 1,000 |
| Megabyte (MB) | 1,000,000 |
| Gigabyte (GB) | 1,000,000,000 |
| Terabyte (TB) | 1,000,000,000,000 |
| Petabyte (PB) | 1,000,000,000,000,000 |

Whether computer-related orders of magnitude are based on 1,000 bytes or 1,024 bytes is not standardised; however, the GCSE course expects them as multiples of 1,000, probably for ease of calculations (I believe the exams are no-calculators-allowed, at least at the time of writing).

**There is always 8 bits in a byte.[^1]**

## 1.3.3 Common types of storage

There are three key types of storage used in modern computers:

### Magnetic storage devices
Magnetic storage devices (e.g. HDDs) use magnetic fields to magnetise tiny sections of a spinning metal disk, each section representing one bit. As the disk is spinning, a read/write *head* moves across its surface; to write data, the head magnetises or demagnetises the section of the disk under it, and to read data, the head interprets whether the section is magnetised or not.

These devices are **cheap**, and **high in capacity**. Whilst they are more durable than optical devices, they can be damaged if they are **dropped**, if they are put near strong **magnets**, or if they change their mind about working (which will inevitably happen at some point).

### Optical devices
Optical storage devices (e.g. CDs, DVDs, and Blu-rays) use a laser to scan the surface of a spinning plastic disc. Flat areas on the disc are known as **lands**, and hollow areas on the disc are known as **pits.** When the laser shines on the disc surface, lands reflect the light back whereas pits scatter the light. Lands represent `1`s, and pits represent `0`s.

There are different types of optical media:
 - **ROM media** act like the optical equivalent of [read-only memory](MEMORY.md#122-read-only-memory-rom); they cannot be written to.
 - **R media** are blank, and can be written to **only once** via the laser burning pits to represent `0`s.
 - **RW media** are blank, similar to R media - however, they can be written to more than once.

### Solid state storage devices
Solid state storage devices (e.g. SSDs and USB sticks) are non-volatile RAM.

These devices are very **durable** *(no moving parts)*, **quick**, **efficient** (they need little power), and **portable** due to their small size and durability. However, these factors make SSDs **very expensive;** for example, a 256GB SSD could cost the same amount as a HDD with several terabytes of capacity.

## 1.3.4 Choosing suitable storage devices for given scenarios using basic characteristics

 - If **capacity** is necessary, a **magnetic storage device** could be considered. Optical devices are a no-go in this case.
 - If **speed** is needed, **solid state devices** should be used.
 - If **portability** is important, **optical devices** should be used (although with sufficient protection from scratches).
 - If **durability** is a must, optical devices should be avoided. Go for magnetic storage, or even better, **solid state storage**.
 - If **reliability** is required, magnetic storage should be avoided. Optical storage is fine, but **solid state storage** is the best option.
 - If **cost** is the deciding factor, then **optical devices** or **magnetic storage devices** should be considered; avoid solid state storage.

## References

### Sections
 - [1.3.1 Secondary storage, also known as storage](https://www.bbc.co.uk/bitesize/guides/z67j2nb/revision/1)
 - [1.3.2 Data capacity](https://www.bbc.co.uk/bitesize/guides/z67j2nb/revision/4)
 - [1.3.3 Common types of storage](https://www.bbc.co.uk/bitesize/guides/z67j2nb/revision/2)

[^1]: https://stackoverflow.com/a/53939806/12980669
