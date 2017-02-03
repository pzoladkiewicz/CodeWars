Write a ```reverseWords``` function that accepts a string a parameter, and reverses each word in the string. Every space should stay, so you cannot use ```words``` from ```Prelude```.

Example:
```
reverse_words("This is an example!") # returns  "sihT si na !elpmaxe"
```
```python
def reverse_words(str):
    return ' '.join(w[::-1] for w in str.split(' '))
```
