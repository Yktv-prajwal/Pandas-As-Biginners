
# PANDAS SERIES NOTES


# 1. Import Pandas
import pandas as pd

# Pandas is a Python library used for data analysis and manipulation.

# Check Version
print(pd.__version__)

# ---------------------------
# 2. Create a Series from List
# ---------------------------
data = ["java", "c++", "ruby", "go", "jsp", "julia", "Python"]

s = pd.Series(data)

# Series is a one-dimensional labeled array.
# Default index starts from 0.

print(s)

# ---------------------------
# 3. Create Custom Index
# ---------------------------
data = ["Java", "C++", "Python", "Ruby", "Go", "jsp", "julia"]

indexx = ["a", "b", "c", "d", "e", "f", "g"]

s = pd.Series(data, index=indexx)

print(s)

# Custom index replaces default numeric index.

# ---------------------------
# 4. Create Series from Dictionary
# ---------------------------
data = {
    "a":100,
    "b":300,
    "c":400,
    "d":450
}

s = pd.Series(data)

print(s)

# Dictionary keys become index.
# Dictionary values become Series values.

# ---------------------------
# 5. Access Elements
# ---------------------------

# By Position
print(s[0])

# By Custom Index
print(s["c"])

# Slice
print(s[:3])

# ---------------------------
# 6. Update Index
# ---------------------------
data = ["java","c++","ruby","go"]

indexx = ["a","b","c","d"]

s = pd.Series(data,index=indexx)

print(s)

# ---------------------------
# 7. Series from NumPy Array
# ---------------------------
import numpy as np

data = np.array([11,12,13,14,15])

s = pd.Series(data)

print(s)

# NumPy array can be converted into Pandas Series.

# ---------------------------
# 8. Arithmetic Operations
# ---------------------------

print(s * 2)

# Multiply each element by 2.

print(s + 50)

# Add 50 to every element.

# Pandas performs element-wise operations.

# ---------------------------
# 9. Conditional Filtering
# ---------------------------

print(s[s > 14])

# Returns elements satisfying condition.

# ---------------------------
# Important Pandas Functions
# ---------------------------

# pd.Series()      -> Create Series
# pd.__version__   -> Check version
# s[0]             -> Access by position
# s["a"]           -> Access by label
# s[:3]            -> Slicing
# s*2              -> Multiplication
# s+50             -> Addition
# s[s>14]          -> Filtering

# ---------------------------
# Viva Points
# ---------------------------

# 1. Pandas is used for data analysis.
# 2. Series is a one-dimensional labeled array.
# 3. Default indexing starts from 0.
# 4. Custom indexing can be provided.
# 5. Dictionary keys become Series indexes.
# 6. NumPy arrays can be converted into Series.
# 7. Series supports arithmetic operations.
# 8. Series supports conditional filtering.
# 9. Slicing works like Python lists.
# 10. Pandas automatically aligns data based on index.

# ===========================
# Output Types
# ===========================

# object -> String data
# int64  -> Integer data
# float64 -> Decimal data
# bool   -> Boolean values
