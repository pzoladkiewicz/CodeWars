
Given two integers, which can be positive and negative, find the sum of all the numbers between including them too and return it. If both numbers are equal return a or b.

Note! a and b are not ordered!

Example:  

    get_sum(1, 0) == 1   // 1 + 0 = 1
    get_sum(1, 2) == 3   // 1 + 2 = 3
    get_sum(0, 1) == 1   // 0 + 1 = 1
    get_sum(1, 1) == 1   // 1 Since both are same
    get_sum(-1, 0) == -1 // -1 + 0 = -1
    get_sum(-1, 2) == 2  // -1 + 0 + 1 + 2 = 2  
Waiting for the Feedback! Thanks!
```py
def get_sum(a,b):
    return sum(range(a, b+1) if b > a else range(b, a+1))
```
```py
def get_sum(a,b):
    return sum(range(min(a,b), max(a,b)+1))
```
