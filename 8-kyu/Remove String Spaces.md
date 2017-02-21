Simple, remove the spaces from the string, then return the resultant string.
```python
def no_space(x):
    #return ''.join(l for l in x if l != ' ' )
    return x.replace(' ', '')
```
