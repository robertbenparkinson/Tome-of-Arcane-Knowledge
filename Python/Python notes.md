# Python Basics

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

