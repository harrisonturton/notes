# Assembly Reference

Computers run on 1s and 0s, but writing binary code _sucks_. To help this, the Assembly language was created. Assembly instructions have a strong \(but not one-to-one\) correlation to compiled machine code. In many cases, an instruction is a simple moniker for a binary operation code \(opcode\).

This section will provide an overview of assembly programming.

#### Example Program

```
  .syntax unified
  .global main
  .type main, %function

main:
  mov r0, 5   @ Set r0 to 5
  add r0, 3   @ Add 3 to r0 (Now 8)
  cmp r0, 8   @ Compare r0 to 8
  beq finish  @ If equal, branch to "finish"
  mov r3, 5   @ Set r3 to 5
finish:
  nop         @ Don't do anything
  b finish    @ Branch to "finish"
```



