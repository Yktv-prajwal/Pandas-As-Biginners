# Pandas Series - Lecture Notes

## Introduction
**Pandas** is a powerful Python library used for data analysis and data manipulation.

```python
import pandas as pd
```

Check the installed version:

```python
print(pd.__version__)
```

---

# 1. Pandas Series

A **Series** is a one-dimensional labeled array capable of holding data of any type.

## Creating a Series from a List

```python
import pandas as pd

data = ["java", "c++", "ruby", "go", "jsp", "julia", "Python"]

s = pd.Series(data)

print(s)
```

### Output

```
0      java
1       c++
2      ruby
3        go
4       jsp
5     julia
6    Python
dtype: object
```

---

# 2. Custom Index

We can assign our own index labels.

```python
data = ["Java", "C++", "Python", "Ruby", "Go", "jsp", "julia"]

indexx = ["a", "b", "c", "d", "e", "f", "g"]

s = pd.Series(data, index=indexx)

print(s)
```

### Output

```
a      Java
b       C++
c    Python
d      Ruby
e        Go
f       jsp
g     julia
dtype: object
```

---

# 3. Series from Dictionary

Dictionary keys become indexes and values become Series values.

```python
data = {
    "a": 100,
    "b": 300,
    "c": 400,
    "d": 450
}

s = pd.Series(data)

print(s)
```

### Output

```
a    100
b    300
c    400
d    450
dtype: int64
```

---

# 4. Accessing Data

## By Position

```python
print(s[0])
```

## By Label

```python
print(s["c"])
```

## Slicing

```python
print(s[:3])
```

---

# 5. Series from NumPy Array

```python
import numpy as np

data = np.array([11, 12, 13, 14, 15])

s = pd.Series(data)

print(s)
```

### Output

```
0    11
1    12
2    13
3    14
4    15
dtype: int64
```

---

# 6. Arithmetic Operations

## Multiplication

```python
print(s * 2)
```

### Output

```
22
24
26
28
30
```

## Addition

```python
print(s + 50)
```

### Output

```
61
62
63
64
65
```

---

# 7. Conditional Filtering

```python
print(s[s > 14])
```

### Output

```
4    15
dtype: int64
```

---

# Important Pandas Functions

| Function | Description |
|----------|------------|
| `pd.Series()` | Create a Series |
| `pd.__version__` | Check Pandas version |
| `s[0]` | Access by position |
| `s["a"]` | Access by label |
| `s[:3]` | Slice Series |
| `s * 2` | Multiply elements |
| `s + 50` | Add value to elements |
| `s[s > 14]` | Filter data |

---

# Data Types

| Type | Meaning |
|------|----------|
| object | String Data |
| int64 | Integer Data |
| float64 | Decimal Data |
| bool | Boolean Data |

---

# Viva Questions

### What is Pandas?
Pandas is a Python library used for data analysis and manipulation.

### What is a Series?
A Series is a one-dimensional labeled array.

### What is the default index in a Series?
The default index starts from 0.

### Can we use custom indexes?
Yes, custom indexes can be assigned.

### Can a dictionary be converted into a Series?
Yes, dictionary keys become indexes and values become Series values.

### Can a NumPy array be converted into a Series?
Yes, using `pd.Series()`.

### Does Series support arithmetic operations?
Yes, element-wise arithmetic operations are supported.

### What is conditional filtering?
Selecting values based on a condition.

Example:

```python
s[s > 14]
```

---

# Key Points

- Pandas is used for data analysis.
- Series is one-dimensional.
- Default indexing starts from 0.
- Custom indexing is possible.
- Dictionaries can create Series.
- NumPy arrays can create Series.
- Arithmetic operations are element-wise.
- Conditional filtering is supported.
- Series can store different data types.
- Pandas automatically manages indexes.

---

## Author
**Prajwal Kumbhar**
