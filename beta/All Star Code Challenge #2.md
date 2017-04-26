**This Kata is intended as a small challenge for my students**

All Star Code Challenge #2

Create a function, named findAverage, that takes an array of ages of All Star Code students and returns the average (do NOT round the return value).
```
allStars = [1, 9, 2, 8, 10]
findAverage(allStars) # => 30/5 = 6
```
```python
def findAverage(allStars):
    return sum(allStars) / len(allStars)
```
