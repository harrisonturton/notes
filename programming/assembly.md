# Assembly Reference

Computers run on 1s and 0s, but writing binary code _sucks_. To help this, the Assembly language was created. Assembly instructions have a strong \(but not one-to-one\) correlation to compiled machine code. In many cases, an instruction is a simple moniker for a binary operation code \(opcode\).

#### Registers

A register is a place to store information. There are 16 labelled registers we can use, from `r0` to `r16`. A common pattern is to load data into registers, perform operations, and then saving this data back to memory. Registers are convenient & fast for the CPU to use.

Note: all 'information' is binary, and can be thought of as a number.

#### Program Status Register \(PSR\)

So each register has 32 bits. If I were to add two \(large\) 32-bit numbers together, how could I store the result? Well, I couldn't. This is an _carry_, which means the result has "carried over" into a larger number of bits. As long as we know a carry has occured, we can store this large value in a 32 bit number.

The _Program Status Register _\(PSR\) tells us about what happened when an operation was performed. It may have:

1. Become Negative
2. Become Zero
3. Carried \(Gone above a 32-bit number\)
4. Overflowed \(Gone from the negative to positive space, or vice versa\)

These are the **NZCV **flags, and are **only set if the instruction has the "s" suffix**.

#### Simple Operations

##### **mov**

The `mov` instruction loads/replaces data in a register.

```
mov{s}<c><q> <Rd>, <Rm>
mov{s}<c><q> <Rd>, #<const>
```

```
mov r0, 3    @ r0 now holds 3 in binary, or "11"
mov r1, r0   @ r1 now holds what was in r0 - "11"
```

**add**

The `add` instruction adds to the number in the register.

```
adds{s}<c><q> {<Rd>,} <Rn>, <Rm> {, <shift>}
```

```
mov r0, 5    @ Load 5 into r0
add r0, 3    @ Add 3 to r0, which is now 5.
```

#### Labelling & Branching

Assembler is a linear language, i.e. the instructions run from top to bottom. This is pretty restrictive -- how do we perform loops? This is where labelling & branching comes in handy. 

```
main:
    mov r0, 0    @ Init r0 with 0
loop:
    add r0, 1    @ Increment r0
    b loop       @ Jump to beginning of loop
```



