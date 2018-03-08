# Memory

### **RAM**

RAM \(Random Access Memory\) is for storing large amounts of data. There are two types of RAM -- **static **\(SRAM\) and **dynamic **\(DRAM\).

| **Static RAM \(SRAM\)** | **Dynamic Ram \(DRAM\)** |
| :--- | :--- |
| Fast | Slow |
| Power-hungry | Efficient |
| Physically Larger \(Big bois\) | Physically Dense \(Small bois\) |
| Used where performance is critical \(e.g. caches\). | Used where low-cost & capacity is critical. |
|  | Common in consumer hardware |

### Addressable Units

A byte is the \_smallest addressable unit, \_i.e. we can only uniquely identify bytes. We have 8-bit bytes, so each memory address points to 8 bits.

The Discoboard CPU is 32-bit, meaning it has 32-bit addresses. This means we **can only address 2^32 bytes, or 4GB. **This is why most hardware has moved to 64-bit architectures.

### Memory Segmentation

First & foremost, the **Linker **swaps out labels & memory addresses. It also ensures that certain parts of your program are put into the right address space, ensuring:

* Secret data isn't readable
* Code/instructions aren't writable
* 'Storage' memory isn't executable

### Load & Store Instructions

**Load**

```
ldr<c><q> <Rd>, [<Rb> {, #+-/-<offset>}]
```

```
ldr r0, [r1] @ Read the 32-bit at memory address [r1] into r0
```

`ldr` loads the data from a memory address into a register.** Registers in square brackets are interpreted as memory addresses.**

**Store**

```
str<c><q> <Rs>, [<Rb> {, #+/-<offset>}]
```

```
str r0, [r1] @ Store the data in r0 at the memory address [r1]
```

`str` takes data in a register and stores it at a memory address.

### ARM Cortex-M Memory Diagram

### ![](/assets/Screen Shot 2018-03-08 at 10.38.52 pm.png)

### ![](/assets/Screen Shot 2018-03-08 at 10.38.52 pm.png)



