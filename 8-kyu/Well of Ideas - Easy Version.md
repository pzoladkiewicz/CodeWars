For every good kata idea there seem to be quite a few bad ones!

In this kata you need to check the provided array (x) for good ideas 'good' and bad ideas 'bad'. If there are one or two good ideas, return 'Publish!', if there are more than 2 return 'I smell a series!'. If there are no good ideas, as is often the case, return 'Fail!'.
```python
def well(x):
    g = x.count('good')
    if g == 0: return 'Fail!'
    elif g < 3: return 'Publish!'
    return 'I smell a series!'
```
```python
def well(a):
    c=a.count('good')
    return['Fail!','Publish!','I smell a series!'][(c>0)+(c>2)]
```
