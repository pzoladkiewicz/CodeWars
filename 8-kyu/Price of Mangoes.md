There's a 3 for 2 offer on mangoes. For a given price and quantity, calculate the total cost of the mangoes.
```py
def mango(quantity, price):
    return ((quantity//3)*2 + (quantity%3)) * price
```
```py
def mango(quantity, price):
    return (quantity - quantity // 3) * price
```
