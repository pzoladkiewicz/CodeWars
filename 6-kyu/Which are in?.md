Given two arrays of strings ``a1`` and ``a2`` return a sorted array r in lexicographical order of the strings of a1 which are substrings of strings of ``a2``.

Example 1:
```
a1 = ["arp", "live", "strong"]
a2 = ["lively", "alive", "harp", "sharp", "armstrong"]
```
returns ```["arp", "live", "strong"]```

Example 2:
```
a1 = ["tarp", "mice", "bull"]
a2 = ["lively", "alive", "harp", "sharp", "armstrong"]
```
returns ```[]```

Notes:

Arrays are written in "general" notation. See "Your Test Cases" for examples in your language.

Beware: ``r`` must be without duplicates.

```py
def in_array(array1, array2):
    ret = []
    for i in array1:
        for j in array2:
            if i in j:
                if i not in ret: ret.append(i)
                
    return sorted(ret)

```
```py
def in_array(a1, a2):
    return sorted({sub for sub in a1 if any(sub in s for s in a2)})
```
