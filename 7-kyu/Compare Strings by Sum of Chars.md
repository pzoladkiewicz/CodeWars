Compare two strings by comparing the sum of their values (ASCII character code).
For comparing treat all letters as UpperCase.

Null-Strings should be treated as if they are empty strings.
If the string contains other characters than letters, treat the whole string as it would be empty.

Examples:

"AD","BC" -> equal

"AD","DD" -> not equal

"gf","FG" -> equal

"zz1","" -> equal

"ZzZz", "ffPFF" -> equal

"kl", "lz" -> not equal

null, "" -> equal

Your method should return true, if the strings are equal and false if they are not equal.

```py
def compare(s1,s2):
    if s1 == '' or s2 == '': return True
    s1Val = sum(ord(l.upper()) for l in s1 if s1.isalpha())
    s2Val = sum(ord(l.upper()) for l in s2 if s2.isalpha())
    return s1Val == s2Val
```
