You will be provided 3 numbers. num1, num2 and a target number target. Your job is to write a program that will return the corect opratar to get num1 and num2 to the target oprator.

it can return either: add, subtract, multiply or divide apropriatly.
```python
def get_op(num1, num2, target):
    if num1 + num2 == target:
        return 'add'
    elif num1 - num2 == target:
        return 'subtract'
    elif num1 * num2 == target:
        return 'multiply'
    else:
        return 'divide'
```
