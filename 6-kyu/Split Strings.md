Complete the solution so that it splits the string into pairs of two characters. If the string contains an odd number of characters then it should replace the missing second character of the final pair with an underscore ('_').

Examples:
```py
solution('abc') # should return ['ab', 'c_']
solution('abcdef') # should return ['ab', 'cd', 'ef']
```
```py
def solution(s):
    output = []
    for l in range(0, len(s), 2):
        temp = s[l:l+2]
        if len(temp) == 2:
            output.append(temp)
        else:
            output.append(temp + '_')

    return output
```
```py
def solution(s):
    return [(s + "_")[i:i + 2] for i in range(0, len(s), 2)]
```
```py
def solution(s):
    return [s[x:x+2] if x < len(s) - 1 else s[-1] + "_" for x in range(0, len(s), 2)]
```
