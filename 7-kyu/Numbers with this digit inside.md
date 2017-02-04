You have to search all numbers from inclusive 1 to inclusive a given number x, that have the given digit d in it.
The value of d will always be 0 - 9.
The value of x will always be greater than 0.

You have to return as an array
* the count of these numbers,
* their sum
* and their product.

For example:
```
x = 11
d = 1
->
Numbers: 1, 10, 11
Return: [3, 22, 110]
```

If there are no numbers, which include the digit, return [0,0,0].

Have fun coding it and please don't forget to vote and rank this kata! :-)

I have created other katas. Have a look if you like coding and challenges.
```python
def numbers_with_digit_inside(x, d):
    count = 0
    suma = 0
    product = 1
    for n in range(1, x+1):
        if str(d) in str(n):
            count += 1
            suma += n
            product *= n
    if count == 0:
        return [0, 0, 0]
    else:
        return [count, suma, product]
 ```
