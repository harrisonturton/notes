# Branching

Assembler is a linear language, i.e. the instructions run from top to bottom. This is pretty restrictive -- how do we perform loops? This is where labelling & branching comes in handy.

```assembly
main:
  mov r0, 0    @ Init r0 with 0
loop:
  add r0, 1    @ Increment r0
  b loop       @ Jump to beginning of loop
```

When the program reaches `b loop`, it sets the `pc` register to be `loop`, and so the programs jumps to that location. This creates an infinite loop. We can break out of it but branching to a different statement.

#### Conditional Operations

```assembly
mov r0, 5
cmp r0, 5
beq main
```

#### Subroutines

```
bl subroutine
subroutine:
  ...
  bx lr
```

### Labels & the Linker

```
main:
  add r0, 5
```

Labels are human-readable aliases for memory addresses. If labels didn't exist, we'd have to jump to a specific memory address with an instruction. Whenever our code was changed, we'd have to update all these addresses.

Labels are not present in the machine-code. The **Linker** goes through and swaps labels for memory addresses.



