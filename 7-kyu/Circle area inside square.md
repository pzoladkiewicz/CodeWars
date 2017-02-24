Turn an area of a square in to an area of a circle that fits perfectly inside the square.
Your function gets a number which represents the size of the square and should return the size of the circle. The tests are rounded by 8 decimals to make sure multiple types of solutions work.
You don't have to worry about error handling or negative number input: size >= 0.
```python
import math

def square_area_to_circle(size):
        return math.pi * (size**.5/2)**2
```
```python
import math

def square_area_to_circle(size):
        return math.pi * size/4
```
