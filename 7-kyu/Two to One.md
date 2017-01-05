Take 2 strings ```s1``` and ```s2``` including only letters from ato z. Return a new sorted string, the longest possible, containing distinct letters, - each taken only once - coming from s1 or s2.

Examples:
  
> a = "xyaabbbccccdefww"  
> b = "xxxxyyyyabklmopq"  
> longest(a, b) -> "abcdefklmopqwxy"

> a = "abcdefghijklmnopqrstuvwxyz"  
> longest(a, a) -> "abcdefghijklmnopqrstuvwxyz"

```py
def longest(s1, s2):
    a = ''.join(set(s1))
    b = ''.join(set(s2))
    return ''.join(sorted(set(a + b)))
```
```py
import string

def longest(s1, s2):
    return ''.join(l for l in string.ascii_lowercase if l in s1 or l in s2)
```
```py
def longest(a1, a2):
    return "".join(sorted(set(a1 + a2)))
```
