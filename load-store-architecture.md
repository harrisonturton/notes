# Load / Store Architecture

The CPU interacts with the world through load/store instructions to specific memory addresses, e.g:

* Loading & storing data in RAM
* Configuring peripherals on the board
* Blinking the LEDs

**Load/Store Model: **Treat \_everything \_like memory.

### Not all Memory is Data

Some memory has specific abilities:

* Readable
* Writable
* Executable
* Connected to external peripherals \(which can be w/r/x or a combo\)

Shorthand of **WRX**.

