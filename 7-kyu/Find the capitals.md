Write a function that takes a single string ```(word)``` as argument. The function must return an ordered list containing the indexes of all capital letters in the string.
```py
import string

def capitals(word):
    return [i for i, l in enumerate(word) if l in string.ascii_uppercase]
```
```py
def capitals(word):
    return [i for (i, c) in enumerate(word) if c.isupper()]
```
