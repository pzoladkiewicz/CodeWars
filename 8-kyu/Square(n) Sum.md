Complete the squareSum method so that it squares each number passed into it and then sums the results together.

For example:

    square_sum([1, 2, 2]) # should return 9
```py
def square_sum(numbers):
    return sum(n*n for n in numbers)
```
