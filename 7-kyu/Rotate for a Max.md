Take a number: ```56789```. Rotate left, you get ```67895```.

Keep the first digit in place and rotate left the other digits: ```68957```.

Keep the first two digits in place and rotate the other ones: ```68579```.

Keep the first three digits and rotate left the rest: ```68597```. Now it is over since keeping the first four it remains only one digit which rotated is itself.

You have the following sequence of numbers:

```56789 -> 67895 -> 68957 -> 68579 -> 68597```

and you must return the greatest: ```68957```.

Calling this function max_rot (or maxRot or ... depending on the language)

max_rot(56789) should return ```68957```
```py
def max_rot(n):
    output = [n]
    toRotate = str(n)
    for i in range(len(str(n))-1):
        temp = toRotate[:i]
        temp_2 = toRotate[i:]
        rotated = temp_2[1:] + temp_2[:1]
        output.append(temp + rotated)
        toRotate = temp + rotated
    return max(int(l) for l in output)
```
```py
def max_rot(n):
    s, arr = str(n), [n]
    for i in range(len(s)):
        s = s[:i] + s[i+1:] + s[i]
        arr.append(int(s))
    return max(arr)
```
