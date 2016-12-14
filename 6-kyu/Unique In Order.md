Implement the function unique_in_order which takes as argument a sequence and returns a list of items without any elements with the same value next to each other and preserving the original order of elements.

For example:
```py
unique_in_order('AAAABBBCCDAABBB') == ['A', 'B', 'C', 'D', 'A', 'B']
unique_in_order('ABBCcAD')         == ['A', 'B', 'C', 'c', 'A', 'D']
unique_in_order([1,2,2,3,3])       == [1,2,3]
```
```py
def unique_in_order(iterable):
    if len(iterable) == 0 : return []
    ret = [iterable[0]]
    for i in range(1, len(iterable)):
        print(iterable[i], iterable[i-1])
        if iterable[i] != iterable[i-1]:
            ret.append(iterable[i])
    return ret
```
```py
from itertools import groupby

def unique_in_order(iterable):
    return [k for (k, _) in groupby(iterable)]
```
