# Pandas Day 3 - Data Cleaning

## Topics Covered

1. Missing Values
2. isnull()
3. notnull()
4. fillna()
5. dropna()
6. duplicated()
7. drop_duplicates()
8. rename()
9. astype()
10. replace()

---

# Why Data Cleaning?

Real-world datasets often contain:
- Missing values
- Duplicate records
- Incorrect data types
- Wrong values
- Inconsistent column names

Cleaning data improves analysis accuracy.

---

# 1. isnull()

Checks missing values.

Syntax

```python
df.isnull()
```

Count missing values

```python
df.isnull().sum()
```

---

# 2. notnull()

Returns True for available values.

```python
df.notnull()
```

---

# 3. fillna()

Replaces missing values.

Replace with 0

```python
df.fillna(0)
```

Replace Age with average

```python
df["Age"].fillna(df["Age"].mean())
```

Replace City

```python
df["City"].fillna("Unknown")
```

---

# 4. dropna()

Removes missing values.

Remove rows

```python
df.dropna()
```

Remove columns

```python
df.dropna(axis=1)
```

---

# 5. duplicated()

Checks duplicate rows.

```python
df.duplicated()
```

Count duplicates

```python
df.duplicated().sum()
```

---

# 6. drop_duplicates()

Removes duplicate rows.

```python
df.drop_duplicates()
```

---

# 7. rename()

Rename columns.

```python
df.rename(columns={"Age":"Employee_Age"})
```

Rename multiple columns

```python
df.rename(columns={
"Age":"Employee_Age",
"City":"Location"
})
```

---

# 8. astype()

Changes data type.

```python
df["Age"]=df["Age"].astype(float)
```

String

```python
df["Salary"]=df["Salary"].astype(str)
```

---

# 9. replace()

Replace values.

```python
df.replace("Mumbai","Pune")
```

Replace multiple values

```python
df.replace({
"Mumbai":"Pune",
"Delhi":"Noida"
})
```

---

# Summary

isnull()

notnull()

fillna()

dropna()

duplicated()

drop_duplicates()

rename()

astype()

replace()