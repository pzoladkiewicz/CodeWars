Write a function

```triple_double(num1, num2)```
which takes in numbers ```num1``` and ```num2``` and returns ```1``` if there is a straight triple of a number at any place in ```num1``` and also a straight double of the same number in ```num2```.
For example:
```
triple_double(451999277, 41177722899) == 1 // num1 has straight triple 999s and 
                                          // num2 has straight double 99s
triple_double(1222345, 12345) == 0 // num1 has straight triple 2s but num2 has only a single 2
triple_double(12345, 12345) == 0
triple_double(666789, 12345667) == 1
```
If this isn't the case, return ```0```

    def triple_double(num1, num2):
        n = str(num1)
        m = str(num2)
        for n1 in range(len(n)-2):
            if n[n1] == n[n1+1] and n[n1] == n[n1+2]:
                for m1 in range(len(m)-1):
                    if n[n1] == m[m1] and n[n1] == m[m1+1]:
                        return 1
        return 0

```
def triple_double(num1, num2):
    return any([i * 3 in str(num1) and i * 2 in str(num2) for i in '0123456789'])
```

    def triple_double(num1, num2):
        num1, num2 = str(num1), str(num2)
        for num in '0123456789':
            if num * 3 in num1 and num * 2 in num2:
                return 1
        return 0
        
```
def triple_double(num1, num2):
    for x in range(10):
        if str(x) * 3 in str(num1):
            if str(x) * 2 in str(num2):
                return 1
    return 0

```
