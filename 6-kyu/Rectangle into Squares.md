The drawing below gives an idea of how to cut a given "true" rectangle into squares ("true" rectangle meaning that the two dimensions are different).

    '5x3' rectangle, cut into '3x3', '2x2' and '1x1', '1x1' squares

Can you translate this drawing into an algorithm?

You will be given two dimensions

1. a positive integer length (parameter named lng)
2. a positive integer width (parameter named wdth)

You will return an array with the size of each of the squares.
```
sqInRect(5, 3) should return [3, 2, 1, 1]
sqInRect(3, 5) should return [3, 2, 1, 1]
```
Note:

lng == wdth as a starting case would be an entirely different problem and the drawing is planned to be interpreted with lng != wdth. See kata, Square into Squares. Protect trees!.

When the initial parameters are so that ```lng``` == ```wdth```, the solution ```[lng]``` would be the most obvious but not in the spirit of this kata so, in that case, return ```None/nil/null/Nothing```. Return ```{}``` with C++.

In that case the returned structure of C will have its sz component equal to 0. (See the "Solution" and "Examples" tabs)

    sqInRect(5, 5) should return None
```py
def sqInRect(lng, wdth):
    if lng == wdth: return None
    output = []
    area = lng * wdth
    while area > 0:
        check = int(area ** .5)
        while check > lng or check > wdth:
            check -= 1
        output.append(check)
        area -= check**2
        if lng > wdth:
            lng -= check
        else:
            wdth -= check
    return output
```
```py
def sqInRect(lng, wdth, recur = 0):
    if lng == wdth:
        return (None, [lng])[recur]            # If this is original function call, return None for equal sides (per kata requirement);
                                               # if this is recursion call, we reached the smallest square, so get out of recursion.
    lesser = min(lng, wdth)
    return [lesser] + sqInRect(lesser, abs(lng - wdth), recur = 1)
```
