Write a function, ```calculateTip(amount, rating)``` which calculates how much you need to tip based on the total amount of the bill and the service.

You need to consider the following ratings:
```
Terrible: tip 0%
Poor: tip 5%
Good: tip 10%
Great: tip 15%
Excellent: tip 20%
```
The rating is case insensitive. If an unrecognised rating is input, then you need to return:

```"Rating not recognised"```   in Javascript, Python and Ruby...    
...or ```null``` in Java

Because you're a nice person, you always round up the tip, regardless of the service.
```python
import math

def calculate_tip(amount, rating):
    if rating.lower() in 'terrible':
        return 0
    elif rating.lower() in 'poor':
        return math.ceil(amount * 0.05)
    elif rating.lower() in 'good':
        return math.ceil(amount * 0.1)
    elif rating.lower() in 'great':
        return math.ceil(amount * 0.15)
    elif rating.lower() in 'excellent':
        return math.ceil(amount * 0.2)
    else:
        return 'Rating not recognised'
```
