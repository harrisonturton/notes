# Bitwise Instructions

Not all instructions treat register data as 'numbers' - some treat them like bit vectors \(list of 1s and 0s\).

#### Bitwise Clear

```
mov r1, 0b1111
mov r2, 0b0010
bic r3, r1, r2
r3 == 0b1101
```

`bic` takes two bit vectors. Wherever there is a `1` in the second vector, there will be a `0` in the first.

#### Shifts

**Logical Shift**

```
lsl @ logical shift left
lsr @ logical shift right
```

Logical shifts will 'forget' the bits that drop off, and fill the empties with 0s.

E.g. Shifting `1111` left by 3 becomes `1000`.

**Arithmetic Shift**

```
asr
```

Arithmetic shifts will 'forget' bits that drop off, but fill empties with the last bit.

#### Rotations

```
ror
```

Rotations will 'wrap around', i.e. bits that drop off appear back at the beginning of the bitstring.



