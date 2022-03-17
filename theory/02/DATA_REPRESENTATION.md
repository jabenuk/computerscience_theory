# 2.6 Data representation

## 2.6.1 Data units

Whether data unit orders of magnitude should be in 1,000s or more accurate 1,024s is a fun debate. This course wants them in multiples of 1,000 - not what I would have chosen, but oh well.

| Unit | Size |
| - | - |
| 1 nibble | 4 bits |
| 1 byte B | 8 bits |
| 1 kilobyte KB | 1,000 B |
| 1 megabyte MB | 1,000 KB *(1,000,000 B)* |
| 1 gigabyte GB | 1,000 MB *(1,000,000,000 B)* |
| 1 terabyte TB | 1,000 GB *(1,000,000,000,000 B)* |

## 2.6.2 Signal formats

**Analogue** (or analog when spelt incorrectly) format involves real-life signals that can vary in amplitude, such as sound waves.

**Digital** format is **binary data**, and can only be 1 or 0.

Modern computers require digital data, so a device known as an **analogue-to-digital converter (ADC)** can be used to general digital signals from analogue signals. Conversely, a **digital-to-analogue converter (DAC)** can be used to reverse this process.

## 2.6.3 Numbers

### Binary shifts

Binary numbers can be multiplied and divided via **shifting.**

To multiply a number, a binary shift moves all the digits in the binary number along **to the left** and fills any gaps with 0:
 - to multiply by **2**, all digits shift **1** place to the left
 - to multiply by **4**, all digits shift **2** places to the left
 - to multiply by **8**, all digits shift **3** places to the left

To divide a number, the same is done but **to the right**:
 - to divide by **2**, all digits shift **1** place to the right
 - to divide by **4**, all digits shift **2** places to the right
 - to divide by **8**, all digits shift **3** places to the right

### Check digits

When transmitting data, some errors can occur and data may be incorrectly recieved. To overcome this, an extra value is transmitted to help determine if the data recieved is correct - this is a **check digit.**

The value of the check digit is usually calculated from the rest of the data being sent. For example, the *EAN8* barcode system creates the check digit from the other 7 digits in the barcode:
 1. the first, third, fifth, and seventh numbers are multiplied by 3 and added together
 2. the remaining numbers are added to the total
 3. the total is divided by 10
 4. the check digit is then determined by subtracting the remainder of this division from 10

The check digit of the EAN8 barcode number 2142345 is therefore **1**.

## 2.6.4 Characters

All the characters that a computer can use are called a **character set.** Two standard character sets are:
 - Unicode
 - American Standard Code for Information Interchange (ASCII)
 - Extended ASCII

### ASCII

ASCII uses **seven bits**, giving a character set of 128 characters. The 128 characters include:
 - 32 control codes
 - 32 punctuation codes and symbols + space
 - 26 upper case letters
 - 26 lower case letters
 - numeric digits 0-9

**A** is represented as **65** and **a** is represented as **97.**

### Extended ASCII

Extended ASCII makes use of **eight bits.** So it has a character set of 256 characters.

### Unicode

Unicode uses **sixteen bits**, giving a range of 65,536 characters.

## 2.6.5 Images

Each pixel in an image is represented by a binary number.

### Colour depth

To add colour, more bits are required for each pixel. The number of bits determines the range of colour - this is the **colour depth**. For example, a colour depth of **two** means two **bits per pixel** which means **four** possible colours. 16 bits per pixel means 65,536 possible colours.

The **size of an image file** can be estimated by using the image width, height, and colour depth (bits per pixel). The higher the width, height, or colour depth, the greater the size of the image file.

### Resolution

The **resolution** of an image is a way of describing how tightly packed the pixels are. In low-resolution images, the pixels are larger and therefore fewer are needed to fill the space.

### Metadata

Files contain extra data called **metadata.** Metadata includes data about the file itself, including file size, date created, author. An image file also includes metadata about the image data, such as width, height, resolution, and colour depth. Without this metadata, the image could not be correctly displayed.

## 2.6.6 Sound

An [ADC](#262-signal-formats) will capture a sound wave at regular time intervals. This recording is known as a **sample.** The sound recorded at each sample point is converted to its nearest numeric equivalent, which is then stored in a file.

### Sample rate

The **sample rate** (in Hz) is the number of samples recorded in any given period of time. The higher the sample rate, the closer the recorded signal is to the original. The higher the sample rate, the larger the resulting file. An audio file can normally be recorded at around 44 kHz for good sound quality while keeping a sensible file size.

### Bit depth

**Bit depth** refers to the number of bits used to record each sample, like colour depth in images. Typical bit depths are 16 bit and 24 bit.

### Bit rate

**Bit rate** is simply a measure of how much data is processed for each second of sound. The bit rate is the **sample rate multiplied by the bit depth.**

The higher the bit rate, bit depth, and sample rate, the greater the quality of sound.

## 2.6.7 Compression

Compression can solve problems related to files taking up too much storage space.

### Lossy compression

With **lossy compression**, some data is removed and discarded, thereby reducing the overall size of the file. For example, an image can be compressed by reducing its [colour depth](#colour-depth). Similarly, an audio file can be compressed by reducing its [bit depth](#bit-depth). Various lossy file standards exist:
 - the **JPEG** file format works on this principle
 - the **MPEG** file format (*mp4* and *mp3*) compresses audio and video with lossy compression

### Lossless compression

There are some files where data must not be lost. For example, text files, spreadsheets, emails, etc. Lossless compression reduces file size without losing data, although it is not quite as effective as lossy compression. Various lossless standards exist:
 - **PDF** allows lossless compression of text documents
 - **GIF** is a lossless image file format

One method of lossless compression is **run length encoding (RLE).** With RLE, any consecutive runs of the same data are stored as one item of data instead of many. RLE records what the data is and how many times in succession it occurs. See the following conversion:

`00000011111111000000` *(20 chars)* becomes `608160` *(6 chars)* - six 0s, eight 1s, and another six 0s.

## References

### Sections
 - [2.6.1 Data units](https://www.bbc.co.uk/bitesize/guides/zfspfcw/revision/1)
 - [2.6.2 Signal formats](https://www.bbc.co.uk/bitesize/guides/zfspfcw/revision/1)
 - [2.6.3 Numbers](https://www.bbc.co.uk/bitesize/guides/zfspfcw/revision/2)
 - [2.6.4 Characters](https://www.bbc.co.uk/bitesize/guides/zfspfcw/revision/7)
 - [2.6.5 Images](https://www.bbc.co.uk/bitesize/guides/zfspfcw/revision/8)
 - [2.6.6 Sound](https://www.bbc.co.uk/bitesize/guides/zfspfcw/revision/9)
 - [2.6.7 Compression](https://www.bbc.co.uk/bitesize/guides/zfspfcw/revision/10)
