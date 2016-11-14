Take an array and remove every second element out of that array. Always keep the first element and start removing with the next element.

*Example:*
```my_list = ['Keep', 'Remove', 'Keep', 'Remove', 'Keep', ...]```  

None of the arrays will be empty, so you don't have to worry about that!

```py
def remove_every_other(my_list):
    output = []
    for i, e in enumerate(my_list):
        if i%2 == 0:
            output.append(e)
            
    return output
```

```py
def remove_every_other(my_list):
    return my_list[::2]
```
