You are given an odd-length array of integers, in which all of them are the same, except for one single number.

Implement the method stray which accepts such array, and returns that single different number.

The input array will always be valid! (odd-length >= 3)

*Examples:*
```py
[1, 1, 2] => 2  
[17, 17, 3, 17, 17, 17, 17] => 3
```

```py
def stray(arr):
    return int(''.join([str(n) for n in arr if arr.count(n) == 1]))
```
