# Hypothesis Testing

## Null Hypothesis
There is no different between sample_one and sample_two

## Alternative Hypothesis
There is a differne between sample_one and sample_two

# alpha 
\alpha is the threshold you are holding your results too

larger the \alpha (.1) larger the p-value threshold 

lower the \alpah (.000001) lower the p-value threshold

# Test
```python
from scipy import stats
stats.ttest_ind(sample_one, sample_two)
```

lower the p value the more like the results are not caused by chance 







