You need to write a function that reverses the words in a given string. A word can also fit an empty string. If this is not clear enough, here are some examples:
```python
reverse('Hello World') == 'World Hello'
reverse('Hi There.') == 'There. Hi'
```
Happy coding!
```python
def reverse(st):
    return ' '.join(reversed(st.split()))
```
