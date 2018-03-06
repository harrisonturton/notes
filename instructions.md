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



