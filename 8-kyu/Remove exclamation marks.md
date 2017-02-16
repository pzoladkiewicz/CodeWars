Write function removeExclamationMarks which removes all exclamation marks from a given string.
```python
def remove_exclamation_marks(s):
    return ''.join(l for l in s if l != '!')
```
```python
def remove_exclamation_marks(s):
    return s.replace('!', '')
```
