A Narcissistic Number is a number which is the sum of its own digits, each raised to the power of the number of digits.

For example, take 153 (3 digits):

    1^3 + 5^3 + 3^3 = 1 + 125 + 27 = 153

and 1634 (4 digits):

    1^4 + 6^4 + 3^4 + 4^4 = 1 + 1296 + 81 + 256 = 1634

The Challenge:  
Your code must return true or false depending upon whether the given number is a Narcissistic number.  
Error checking for text strings or other invalid inputs is not required, only valid integers will be passed into the function.
```python
def narcissistic( value ):
    output = 0

    for v in str(value):
        output += int(v)**len(str(value))
        
    return True if output == value else False
```
```python

    def narcissistic(value):
        return value == sum(int(x) ** len(str(value)) for x in str(value))
```
```python       
def narcissistic(value):
    return bool(value==sum([int(a) ** len(str(value)) for a in str(value)]))
```
