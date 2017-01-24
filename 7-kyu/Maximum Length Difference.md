You are given two arrays ```a1``` and ```a2``` of strings. Each string is composed with letters from ```a``` to ```z```. Let ```x``` be any string in the first array and ```y``` be any string in the second array.

```Find max(abs(length(x) − length(y)))```

If ```a1``` or ```a2``` are empty return ```-1``` in each language except in Haskell where you will return Nothing.

Example:
```
s1 = ["hoqq", "bbllkw", "oox", "ejjuyyy", "plmiis", "xxxzgpsssa", "xxwwkktt", "znnnnfqknaz", "qqquuhii", "dvvvwz"]
s2 = ["cccooommaaqqoxii", "gggqaffhhh", "tttoowwwmmww"]
mxdiflg(s1, s2) --> 13
```

```python
def mxdiflg(a1, a2):
    if not a1 or not a2: return -1
    
    len_a1_min = min([len(a) for a in a1])
    len_a1_max = max([len(a) for a in a1])
    len_a2_min = min([len(a) for a in a2])
    len_a2_max = max([len(a) for a in a2])
    
    
    if abs(len_a1_min - len_a2_max) > abs(len_a2_min - len_a1_max):
        return abs(len_a1_min - len_a2_max)
    else:
        return abs(len_a2_min - len_a1_max)
```
```python
def mxdiflg(a1, a2):
    if a1 and a2:
        return max(abs(len(x) - len(y)) for x in a1 for y in a2)
    return -1
```
```python
def mxdiflg(a1, a2):
    if a1 and a2:
        return max(
            len(max(a1, key=len)) - len(min(a2, key=len)),
            len(max(a2, key=len)) - len(min(a1, key=len)))
    return -1
```
