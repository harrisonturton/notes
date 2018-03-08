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



#### Rotations



