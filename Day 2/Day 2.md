# Pandas Day 2 - Selecting & Filtering Data

## Topics Covered

1. Selecting Single Column
2. Selecting Multiple Columns
3. Selecting Rows
4. loc[]
5. iloc[]
6. Boolean Indexing
7. Multiple Conditions
8. isin()
9. between()
10. query()

---

# 1. Selecting a Single Column

A single column can be selected using square brackets.

Syntax

```python
df["Column_Name"]
```

Example

```python
df["Age"]
```

Returns a Pandas Series.

---

# 2. Selecting Multiple Columns

Syntax

```python
df[["Column1","Column2"]]
```

Example

```python
df[["Name","Salary"]]
```

Returns a DataFrame.

---

# 3. Selecting Rows

Display the first 5 rows

```python
df.head()
```

Display last 5 rows

```python
df.tail()
```

---

# 4. loc[]

loc stands for Label Location.

It selects rows and columns using labels.

Syntax

```python
df.loc[row, column]
```

Examples

```python
df.loc[0]

df.loc[0:4]

df.loc[:,["Name","Salary"]]

df.loc[2,"Name"]
```

---

# 5. iloc[]

iloc stands for Integer Location.

It selects rows and columns using index numbers.

Syntax

```python
df.iloc[row,column]
```

Examples

```python
df.iloc[0]

df.iloc[0:5]

df.iloc[0:5,1:3]

df.iloc[2,1]
```

---

# Difference Between loc and iloc

| loc | iloc |
|------|------|
| Uses labels | Uses index positions |
| End index included | End index excluded |
| Works with names | Works with numbers |

---

# 6. Boolean Indexing

Used for filtering data.

Example

```python
df[df["Age"]>25]
```

Returns rows where Age is greater than 25.

---

# 7. Multiple Conditions

AND

```python
df[(df["Age"]>25) & (df["Salary"]>50000)]
```

OR

```python
df[(df["City"]=="Mumbai") | (df["City"]=="Delhi")]
```

NOT

```python
df[~(df["City"]=="Mumbai")]
```

---

# 8. isin()

Checks multiple values.

Example

```python
df[df["City"].isin(["Mumbai","Pune"])]
```

Equivalent to

```python
City == Mumbai OR City == Pune
```

---

# 9. between()

Checks a range.

Example

```python
df[df["Age"].between(20,30)]
```

Returns

Age >=20 and Age<=30

---

# 10. query()

Filters data using SQL-like syntax.

Example

```python
df.query("Age>25")
```

Multiple conditions

```python
df.query("Age>25 and Salary>50000")
```

---

# Summary

df["Column"]

df[["Col1","Col2"]]

df.loc[]

df.iloc[]

df[df["Age"]>25]

isin()

between()

query()