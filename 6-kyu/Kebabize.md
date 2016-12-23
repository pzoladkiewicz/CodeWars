Modify the kebabize function so that it converts a camel case string into a kebab case.

    kebabize('camelsHaveThreeHumps') // camels-have-three-humps
    kebabize('camelsHave3Humps') // camels-have-humps
Notes: - the returned string should only contain lowercase letters

```py
def kebabize(string):
    out = ''
    for l in string:
        if l.isupper():
            out += '-' + l.lower()
        elif l.isdigit():
            pass
        else:
            out += l
    if len(out) == 0:
        return out
    elif out[0] != '-':
        return out
    else:
        return out[1:]
```
