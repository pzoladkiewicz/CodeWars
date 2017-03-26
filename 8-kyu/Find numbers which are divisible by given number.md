Write a function which takes two arguments and returns all number, which are divisible by given divisor. First argument is array of numbers and the second is divisor.
Example
```
divisible_by([1,2,3,4,5,6], 2) == [2,4,6]
```
```python
def divisible_by(numbers, divisor):
    return [n for n in numbers if n%divisor == 0]
```
