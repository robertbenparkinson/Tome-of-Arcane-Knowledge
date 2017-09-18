# Python Basics

## A better way to print things

```python
x = 10
y = 4
s = 'I ate ' + repr(x*y) + ' doughnuts!'
print(s)

# 'I ate 40 doughnuts!'
```
## Add Comas to a string

```python
x = 25937424601
print('{0:,d}'.format(x) )

# 25,937,424,601
```

## 2 Decimal Places

```python
x = 3.1415926	
print('{:.2f}'.format(x) )
```

## Stats

```python
import numpy as np
istribution = np.random.normal(.75, size=1000)

np.std(distribution)

import scipy.stats as stats
stats.kurtosis(distribution)

# a more negative result, the more flat the distribution  
# a more postive result, the more pointy the distriubiton  

stats.skew(distribution)
# smaller the result, smaller the skew 

```


# Pandas

```python

  import pandas as pd
  
  ##makes data.frame called df
  d = [0,1,2,3,4,5,6,7,8,9]
  df = pd.DataFrame(d)
  
  ##add column name
  df.columns =['what ever we want to call them']
  
  ##add new column
  df['New Column']
  
  ##delet column
  del df['New Column']
  
  ##change index names
  i = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
  df.index = i
  
  ##loc function, selects row 'a'
  df.loc['a']
  
  selects rows 'a', 'b', 'c'
  df.loc['a':'c']
  
  ##iloc function
  df.iloc[0:3]
  
  ##select column
  df['column name']
  
  ##select two columns
  df[['column name', 'that other column']]
  
  ##ix function 
  df.ix[5, 'that other column']
  
  ##upto row five, and both columns
  df.ix[:5, [['column name', 'that other column']]
   
```

## Pyplot
```{python}
import matplotlib.pyplot as plt
plt.plot([1,2,3,4])
plt.ylabel('some numbers')
plt.show()
```

### ply.matshow
a simple 64*64 matrix  

```{python}
import matplotlib.pyplot as plt
import numpy as np

plt.matshow(np.random.rand(64, 64), fignum=100, cmap=plt.cm.flag)
plt.show()
```

## Convert Index into date_time 
```{python}
import pandas as pd
df.index = pd.to_datetime(df.index)
```


