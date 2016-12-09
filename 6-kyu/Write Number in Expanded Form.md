You will be given a number and you will need to return it as a string in Expanded Form. For example:

    expanded_form(12) # Should return '10 + 2'
    expanded_form(42) # Should return '40 + 2'
    expanded_form(70304) # Should return '70000 + 300 + 4'  
NOTE: All numbers will be whole numbers greater than 0.

```py
def expanded_form(num):
    ret = []
    for i, n in enumerate(reversed(str(num))):
        if int(n):
            ret.append(str(int(n)*10**i))

    return ' + '.join(reversed(ret))
```
