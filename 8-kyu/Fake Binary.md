Given a string of numbers, you should replace any number below 5 with '0' and any number 5 and above with '1'. Return the resulting string.
```py
    def fake_bin(x):

        for i, n in enumerate(x):
            if int(n) > 4:
                x += '1'
            else:
                x += '0'

        return (x[len(x)//2:])
```        
```py
def fake_bin(x):
    return ''.join('0' if c < '5' else '1' for c in x)
```
