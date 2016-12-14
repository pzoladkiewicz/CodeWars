Given and array of integers (x), return the result of multiplying the values together in order. Example:

```[1, 2, 3] --> 6```  
For the beginner, try to use the reduce method - it comes in very handy quite a lot so is a good one to know.

Array will not be empty.
```py
def grow(arr):
    ret = 1
    for n in arr:
        ret *= n
    return ret
```
