Return the number (count) of vowels in the given string.

We will consider *a, e, i, o*, and *u* as vowels for this Kata.

```py
def getCount(inputStr):
    return len([inputStr.count(l) for l in inputStr if l in 'aeiou'])
```

```py
def getCount(inputStr):
    return sum(1 for let in inputStr if let in "aeiouAEIOU")
```
