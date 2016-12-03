Build Tower by the following given argument:
number of floors (integer and always greater than 0).

Tower block is represented as *

    Python: return a list;
    JavaScript: returns an Array;
    C#: returns a string[];
    PHP: returns an array;
    C++: returns a vector<string>;
    Haskell: returns a [String];

Have fun!

for example, a tower of 3 floors looks like below

    [
      '  *  ', 
      ' *** ', 
      '*****'
    ]

and a tower of 6 floors looks like below

    [
      '     *     ', 
      '    ***    ', 
      '   *****   ', 
      '  *******  ', 
      ' ********* ', 
      '***********'
    ]
```py
def tower_builder(n_floors):
    tower = []
    floor = ''

    for f in range(n_floors):
        stars = '*' * (f*2 + 1)
        spaces = ' ' * (n_floors - f - 1)
        floor = spaces + stars + spaces
        tower.append(floor)
        
    return tower
```
```py
def tower_builder(n):
    return [("*" * (i*2-1)).center(n*2-1) for i in range(1, n+1)]
```
