Complete the bool_to_word (Javascript: boolToWord ) method.

Given: a boolean value

Return: a 'Yes' string for true and a 'No' string for false
```python
def bool_to_word(bool):
    return 'Yes' if bool else 'No'
```
```python
def bool_to_word(bool):
    return ['No', 'Yes'][bool]
```
