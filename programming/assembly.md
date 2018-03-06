# Assembly Reference

Computers run on 1s and 0s, but writing binary code _sucks_. To help this, the Assembly language was created. Assembly instructions have a strong \(but not one-to-one\) correlation to compiled machine code. In many cases, an instruction is a simple moniker for a binary operation code \(opcode\).

#### Registers

A register is a place to store information. There are 16 labelled registers we can use, from `r0` to `r16`. A common pattern is to load data into registers, perform operations, and then saving this data back to memory. Registers are convinient & fast for the CPU to use.

Note: all 'information' is binary, and can be thought of as a number.

#### Flags



#### Operations

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



