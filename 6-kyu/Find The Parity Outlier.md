You are given an array (which will have a length of at least 3, but could be very large) containing integers. The array is either entirely comprised of odd integers or entirely comprised of even integers except for a single integer N. Write a method that takes the array as an argument and returns N.

For example:

    [2, 4, 0, 100, 4, 11, 2602, 36]

Should return: 11

    [160, 3, 1719, 19, 11, 13, -21]

Should return: 160

```py
def find_outlier(integers):
    
    isEven = [n for n in integers if n%2 == 0]

    if len(isEven) == 1:
        return sum(isEven)
    else:
        return sum([n for n in integers if n%2 != 0])
```
```py
def find_outlier(int):
    odds = [x for x in int if x%2!=0]
    evens= [x for x in int if x%2==0]
    return odds[0] if len(odds)<len(evens) else evens[0]
```
