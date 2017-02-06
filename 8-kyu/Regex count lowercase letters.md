Your task is simply to count the total number of lowercase letters in a string.
```python
def lowercase_count(strng):
    return sum(1 for x in strng if 'a' <= x <= 'z')
```
```python
def lowercase_count(strng):
    return sum('a' <= x <= 'z' for x in strng)
```
```python
def lowercase_count(strng):
    return sum(a.islower() for a in strng)
```
