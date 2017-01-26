Your task is to make function, which returns the sum of a sequence of integers.

The sequence is defined by 3 non-negative values: begin, end, step.

If begin value is greater than the end, function should returns 0

```python
def sequence_sum(begin_number, end_number, step):
    return sum(n for n in range(begin_number, end_number+1, step))
```
```python
def sequence_sum(start, end, step):
    return sum(range(start, end+1, step))
```
