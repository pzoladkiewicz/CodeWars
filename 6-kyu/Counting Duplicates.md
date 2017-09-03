Count the number of Duplicates

Write a function that will return the count of _distinct_ case-insensitive alphabetic characters that occur more than once in the input string. The input string can be assumed to contain only alphanumeric characters, including digits, uppercase and lowercase alphabets.

Example

"abcde" -> ```0 # no characters repeats more than once```  
"aabbcde" -> ```2 # 'a' and 'b'```  
"aabbcdeB" -> ```2 # 'a' and 'b'```  
"indivisibility" -> ```1 # 'i'```  
"Indivisibilities" -> ```2 # 'i' and 's'```
```python
def duplicate_count(text):
    # Your code goes here
    check = text.lower()
    output = 0
    for l in check:
      if check.count(l) > 1:
        check = check.replace(l, '')
        output += 1
    return output
```   
```python
def duplicate_count(s):
  return len([c for c in set(s.lower()) if s.lower().count(c)>1])
```
```python
from collections import Counter

def duplicate_count(text):
    return sum(1 for c, n in Counter(text.lower()).iteritems() if n > 1)
```
