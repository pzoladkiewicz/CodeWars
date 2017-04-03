Consider an array of sheep where some sheep may be missing from their place. We need a function that counts the number of sheep present in the array (true means present).

For example,

    [True,  True,  True,  False,
      True,  True,  True,  True ,
      True,  False, True,  False,
      True,  False, False, True ,
      True,  True,  True,  True ,
      False, False, True,  True]
The correct answer would be 17.

```python
def count_sheeps(arrayOfSheeps):
    return sum(arrayOfSheeps)
```

Hint: Don't forget to check for bad values like null/undefined

```python
def count_sheeps(arrayOfSheeps):
    count = 0
    for el in arrayOfSheeps:
        if el:
            count += 1
    return count
```      
```python
def count_sheeps(arrayOfSheeps):
  return arrayOfSheeps.count(True)
```
```python
def count_sheeps(arrayOfSheeps):
  return len([x for x in arrayOfSheeps if x])
```
