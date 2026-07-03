# Pandas Day 1 - Introduction

## What is Pandas?

Pandas is an open-source Python library used for data manipulation and analysis.
It provides powerful data structures such as Series and DataFrame.

---

## Why Pandas?

- Easy to read datasets
- Fast data manipulation
- Data cleaning
- Data analysis
- Works well with NumPy and Matplotlib

---

## Series

A Series is a one-dimensional labeled array.

Syntax:

```python
pd.Series(data)
```

Example:

```python
marks = pd.Series([80,90,95])
```

---

## DataFrame

A DataFrame is a two-dimensional table.

Syntax

```python
pd.DataFrame(data)
```

Example

```python
data={
    "Name":["Rahul","Amit"],
    "Age":[22,25]
}

df=pd.DataFrame(data)
```

---

## read_csv()

Reads a CSV file.

```python
pd.read_csv("employees.csv")
```

---

## head()

Returns first 5 rows.

```python
df.head()
```

---

## tail()

Returns last 5 rows.

```python
df.tail()
```

---

## shape

Returns

```
(rows, columns)
```

Example

```
(500,10)
```

---

## info()

Shows

- Rows
- Columns
- Datatypes
- Missing values

---

## describe()

Shows

- Count
- Mean
- Min
- Max
- Quartiles
