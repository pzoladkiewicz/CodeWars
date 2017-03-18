This time no story, no theory. The examples below show you how to write function accum:

Examples:
```python
accum("abcd")    # "A-Bb-Ccc-Dddd"
accum("RqaEzty") # "R-Qq-Aaa-Eeee-Zzzzz-Tttttt-Yyyyyyy"
accum("cwAt")    # "C-Ww-Aaa-Tttt"
```
The parameter of accum is a string which includes only letters from a..z and A..Z.
```python
def accum(s):
    return '-'.join(((i+1) * l).title() for i,l in enumerate(s))
```


| I think you are absolutely right. str.capitalize seems to be faster than str.title in almost every test that I have run (except really short strings, < 10 chars). In a simple kata like this one, I'm not sure it will make any sort of a noticeable difference but it's interesting to know!
