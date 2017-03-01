Give you two strings: s1 and s2. If they are opposite, return true; otherwise, return false. Note: The result should be a boolean value, instead of a string.

The opposite means: All letters of the two strings are the same, but the case is opposite. you can assume that the string only contains letters or it's a empty string

Some examples:
```
isOpposite("ab","AB") should return true;
isOpposite("aB","Ab") should return true;
isOpposite("aBcd","AbCD") should return true;
isOpposite("AB","Ab") should return false;
isOpposite("","") should return false;
```
```python
def is_opposite(s1,s2):
    if s1:
        return s1 == s2.swapcase()
    else:
        return False
```
```python
def is_opposite(s1,s2):
    return s1!="" and s1.swapcase() == s2
```
