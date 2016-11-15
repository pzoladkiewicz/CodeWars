You get an array of numbers, return the sum of all of the positives ones.

```Example [1,-4,7,12] => 1 + 7 + 12 = 20```  

*Note: array may be empty, in this case return 0.*

```py
def positive_sum(arr):
    return sum([n for n in arr if n > 0 ])
```
