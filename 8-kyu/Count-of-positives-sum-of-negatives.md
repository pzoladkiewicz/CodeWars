Given an array of integers.

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers.
```py
def count_positives_sum_negatives(arr):
    if not arr:
        return []
    else:
        return [
                len([n for n in arr if n > 0]),
                sum([n for n in arr if n < 0])
                ]
```
```py
def count_positives_sum_negatives(arr):
    return [len([x for x in arr if x > 0])] + [sum(y for y in arr if y < 0)] if arr else []
```
