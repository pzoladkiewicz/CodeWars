Your task is to create a function - ```basicOp()```.

The function should take three arguments - operation(string/char), value1(number), value2(number). The function should return result of numbers after applying chosen operation.

Examples:

    basic_op('+', 4, 7)         # Output: 11
    basic_op('-', 15, 18)       # Output: -3
    basic_op('*', 5, 5)         # Output: 25
    basic_op('/', 49, 7)        # Output: 7
    
```py
import operator
def basic_op(op, value1, value2):
    ops = {
           '+': operator.add,
           '-': operator.sub,
           '*': operator.mul,
           '/': operator.truediv
           }
    operation = ops[op]
    return operation(value1, value2)
```
```py
def basic_op(operator, value1, value2):    
    return eval(''.join([str(value1), operator, str(value2)]))
```
```py
def basic_op(operator, value1, value2):
    return eval("{}{}{}".format(value1, operator, value2))
```
