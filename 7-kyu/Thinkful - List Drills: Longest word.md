Write a function ```longest()``` that takes one argument, a list of words, and returns the length of the longest word in the list.

For example:
```
words = ['simple', 'is', 'better', 'than', 'complex']
longest(words)
7
```
```py
def longest(words):
    return max(len(w) for w in words)
```
