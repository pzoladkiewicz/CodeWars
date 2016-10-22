Given a string S. You have to return another string such that even-indexed and odd-indexed characters of S are grouped and groups are space-separated (see sample below)

Note: 
0 is considered to be an even index. 
All input strings are valid with no spaces

input: '**CodeWars**' output '**CdWr oeas**'

    S[0] = 'C'
    S[1] = 'o'
    S[2] = 'd'
    S[3] = 'e'
    S[4] = 'W'
    S[5] = 'a'
    S[6] = 'r'
    S[7] = 's'

Even indices 0, 2, 4, 6, so we have '**CdWr**' as the first group
odd ones are 1, 3, 5, 7, so the second group is '**oeas**'
And the final string to return is '**Cdwr oeas**'

    def sort_my_string(S):
        o1 = ''
        o2 = ''
        for i, x in enumerate(S):
            if i%2 == 0:
                o1 += x
            else:
                o2 += x
        return o1 + ' ' + o2

```
def sort_my_string(s):
    return '{} {}'.format(s[::2], s[1::2])
```

    def sort_my_string(s):
        return s[::2] + ' ' + s[1::2]
 
``` 
def sort_my_string(S):
    return str(S[0::2] + ' ' + S[1::2])
```

    sort_my_string = lambda s: '{} {}'.format(s[0::2], s[1::2])
