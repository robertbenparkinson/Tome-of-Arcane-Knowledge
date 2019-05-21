# Pandas Package for Python

## Import Statement

```python
import pandas as pd
```

## Buiding a dataframe
```python
df = pd.DataFrame(
    {"a" : [1, 2, 3],     
     "b" : [4, 5, 6],     
     "C" : [7, 8, 9]},
    index = [100, 101, 102])
```

or 

```python

x = [[1,2,3],
     [4,5,6],
     [7,8,9]]

df = pd.DataFrame(x, index=[100, 101, 102], columns=["a", "b", "c"])
```

## Accessing a DataFrame with df.iloc

```python
df.iloc[0,0]
>  1

df.iloc[1,1]
> 5

df.iloc[0:2,0:2]

>    | a | b
 100 | 1 | 2
 101 | 4 | 5 

```

## Accessing a DataFrame with df.loc

```python
df.loc[100]
> a | 1
  b | 2
  c | 3

df.loc[100, "a"]
> 1
```

## Boolean Masking with DataFrames

```python
x = df[df["a"] > 7]
print(x)

>    a  b  c
102  7  8  9 

```

## Import Data from CSV
```Python
df = pd.read_csv('example.csv', sep=',', header=0, index_col='id')
```

## DataFrame Methods

```python

df.head() # retreives the first five
df.head(10) # retreives the first ten
df.tail() # retreives the last five
df.info() # 
len(df) # length of df

```




