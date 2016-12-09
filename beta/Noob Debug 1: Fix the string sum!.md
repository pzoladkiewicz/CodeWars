####Help Johnny!

He can't make his code work!

Easy Code

```py
def add(s1, s2):
    s1 = s1.encode()
    s2 = s2.encode()
    s1 = sum(s1)
    s2 = sum(s1)
    return s1+s2
```


Johnny is trying to make a function that adds the sum of two encoded strings, but he can't find the error in his code! Help him!

```py
def add(s1, s2):
    s1 = sum(ord(c) for c in s1)
    s2 = sum(ord(c) for c in s2)
    
    return s1 + s2
```
```py
def add(s1, s2):
    return sum(ord(x) for x in s1+s2)
```
