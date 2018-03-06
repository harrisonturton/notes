# Registers

A register is a place to store information. There are 16 labelled registers we can use, from `r0` to `r16`. A common pattern is to load data into registers, perform operations, and then saving this data back to memory. Registers are convenient & fast for the CPU to use.

There are a number of 'special' registers, which we will explore here.

#### Program Status Register \(PSR\)

So each register has 32 bits. If I were to add two \(large\) 32-bit numbers together, how could I store the result? Well, I couldn't. This is an _carry_, which means the result has "carried over" into a larger number of bits. As long as we know a carry has occured, we can store this large value in a 32 bit number.

The _Program Status Register _\(PSR\) tells us about what happened when an operation was performed. It may have:

1. Become Negative
2. Become Zero
3. Carried \(Gone above a 32-bit number\)
4. Overflowed \(Gone from the negative to positive space, or vice versa\)

These are the **NZCV **flags, and are **only set if the instruction has the "s" suffix**.

#### Program Counter

How does the computer know which instruction to execute? It checks the `pc` \(program counter\) register, and goes to the data at that point. Every time an instruction is completed, the `pc` register is incremented, and the program performs the next operation.

If we change the `pc` register ourselves we can alter how the program is run.

