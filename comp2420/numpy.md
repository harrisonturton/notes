# NumPy

The package "Numerical Python" \(`numpy`\) is a pacakge required for high performance computing & data analysis.  
It provides:

* A powerful `n-array` object
* Mathematical methods, e.g. linear algebra, fourier transformations, RNGs, etc.

### nd-array

This is the backbone object of NumPy. It is a multidimensional array of **the same **data types \(unlike the standard python list\).

Key differences:

* Homogenous elements
* Fixed size
* More efficient operations than the builtin list

**Support data types:**

* `int8`, `int16`, `int32`, `int64`
* `float16`, `float32`, `float64`, `float128`
* `bool`
* `object`
* `String`
* `Unicode`

```py
import numpy as np

# Creating a 32-bit float
float_32 = np.float32(1.324)
print(float_32, float_32.dtype)

# Creating a 8-bit integer
int_8 = np.int8(565210)
print(int_8, int_8.dtype)
```

### Array Creation

Three different ways to create an array:

1. Convert from a Python `List`
2. Builtin `numpy` methods, e.g. `arange`, `ones`, `zeroes`, etc.
3. Reading arrays from disk

```py
import numpy as np

# Create an 2x3 matrix of zeroes
zeroes = np.zeroes((2, 3))

# Create a 3x8 matrix of ones
ones = np.ones((3, 8))

# Creates a 2x3x4 matrix of random values
random = np.random.random((2,3,4))

# Creates a array of 10 elements, numbered 0-9
zeroToNine = np.arange(10)
```

### Indexing

**Single-dimension indexing  
**This is the same as normal Python `Lists.`

```py
import numpy as np

arr = np.arange(10) # array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
print(arr[0])       # 0
print(arr[3])       # 3
```

**Multi-dimensional indexing  
**Pass multiple values within the array index, e.g. `[1,2]`.

```
arr.shape = (2,5) # converts 1x10 into 2x5
print(arr[1,2])   # 7
```

If you use fewer values than the array's dimension, it gives a subarray:

```
print(arr[1])    # array([0, 1, 2, 3, 4])
```

#### Slicing

Slicing is possible in all dimensions.

```py
arr = np.arange(10)
arr.shape = (2,2,2) # Make 3-dimensional
print(arr[:1,:,:1]) # array([[[0],[2]]])

arr2 = np.arange(10)
print(arr2[0][x<5]) # array([0,1,2,3,4])
```

### Element-wise Operations

Methods performed on an `ndarray` are performed element-wise, i.e. the operation is performed on each element.

```py
import numpy as np

arrA = np.arange(5)
arrB = np.arange(5)
print(arrA + arrB) # array([0,2,4,6,8])

print(10*np.sin(arrA)) # array([ 0., 8.41470985, 9.09297427, 1.41120008, 7.56802495])
```

**Note: **Multiplying two arrays is multiplied element-wise, i.e. this is not matrix multiplication. To perform matrix multiplication, we write `np.dot(arrA, arrB)`.



