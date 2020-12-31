![MRISC64](doc/mrisc64-logo.png)

MRISC64 is the planned 64-bit evolution of [MRISC32](https://github.com/mrisc32), an open source RISC/Vector ISA.

# Features

MRISC64 is expected to be almost identical to MRISC32 (including instructions and instruction encoding), except that the basic data width is 64 bits. Thus the main differences to the MRISC32 ISA are:

* Scalar registers are 64 bits wide.
* Vector register elements are 64 bits wide.
* The following packed modes are supported:
  * 1 x 64 bits (one double word)
  * 2 x 32 bits (two words)
  * 4 x 16 bits (four half-words)
  * 8 x 8 bits (eight bytes)
* The following floating-point types are supported:
  * 64-bit (double-precision)
  * 32-bit (single precision)
  * 16-bit (half precision)
  * 8-bit (quarter precision)

## Required modifications

There are mainly two things that need to be modified to work better with a 64-bit machine:

* Encoding and handling of immediate values.
* The `SHUF` instruction.
