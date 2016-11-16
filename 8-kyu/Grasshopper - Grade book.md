#####Grade book  
Complete the function so that it finds the mean of the three scores passed to it and returns the letter value associated with that grade.

Numerical Score |	Letter Grade  
:---: | :---:
90 <= score <= 100	| 'A'
80 <= score < 90	| 'B'
70 <= score < 80	| 'C'
60 <= score < 70	| 'D'
0 <= score < 60	| 'F'
    
Tested values are all between 0 and 100. Theres is no need to check for negative values or values greater than 100.


```py
def get_grade(*args):

    score = {60: 'F', 70: 'D', 80: 'C', 90: 'B', 101: 'A'}
    
    for k, v in sorted(score.items()):
        if sum(args)/3 < k:
            return v
```

```py
def get_grade(s1, s2, s3):
    return {6:'D', 7:'C', 8:'B', 9:'A', 10:'A'}.get((s1 + s2 + s3) / 30, 'F')
```
