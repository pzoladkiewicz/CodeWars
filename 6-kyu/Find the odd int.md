Given an array, find the int that appears an odd number of times.

There will always be only one integer that appears an odd number of times.

```py
def find_it(seq):
    return max(n for n in seq if seq.count(n) %2 != 0)
```
```py
import operator

def find_it(xs):
    return reduce(operator.xor, xs)
```
