Define ```to_alternating_case(char*)``` such that each lowercase letter becomes uppercase and each uppercase letter becomes lowercase. For example:  
  
     def to_alternating_case(string):
        output = ''

        for l in string:
            if l.isupper():
                output += l.lower()
            else:
                output += l.upper()
        return output

```
def to_alternating_case(string):
    return string.swapcase()
```
