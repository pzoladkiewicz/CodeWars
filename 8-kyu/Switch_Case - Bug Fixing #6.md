Oh no! Timmy's evalObject function doesn't work.
```python
def eval_object(v):
    return {"+": v['a']+v['b'],
            "-": v['a']-v['b'],
            "/": v['a']/v['b'],
            "*": v['a']*v['b'],
            "%": v['a']%v['b'],
            "**": v['a']**v['b'], }.get('operation',1)
```
He uses Switch/Cases to evaluate the given properties of an object, can you fix timmy's function?
```python
def eval_object(v):
    return eval(str(v['a']) + v['operation'] + str(v['b']))
```
```python
def eval_object(v):
    return {"+": v['a']+v['b'],
            "-": v['a']-v['b'],
            "/": v['a']/v['b'],
            "*": v['a']*v['b'],
            "%": v['a']%v['b'],
            "**": v['a']**v['b'], }.get(v['operation'])
```
