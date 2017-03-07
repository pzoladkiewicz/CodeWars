Write a function that takes a list (in Python) or array (in other languages) of numbers, and makes a copy.

Note that you may have troubles if you do not return an actual copy, item by item, not just a pointer or an alias for an existing list or array.

If not list or array is given as a parameter, the function should raise an error.
```python
def copy_list(l):
    return l[:]
```
