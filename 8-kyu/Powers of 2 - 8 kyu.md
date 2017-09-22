Write a function `powersOfTwo` which will return list of all powers of 2 from 0 to n (where n is an exponent).

E.g:
```
n = 0 -> 2^0 -> [1]
n = 1 -> 2^0, 2^1 -> [1,2]
n = 2 -> 2^0, 2^1, 2^2 -> [1,2,4]
```

```python
def powers_of_two(n):
    output = []
    for e in range(n+1):
        output.append(2**e)
    return output
```
```python
def powers_of_two(n):
    return [2**x for x in range(n+1)]
```
