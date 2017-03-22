This is the simple version of Shortest Code series. If you need some challenges, please try the challenge version.

Task:

Find out "B"(Bug) in a lot of "A"(Apple).

There will always be one bug in apple, not need to consider the situation that without bug or more than one bugs.

input: string Array ```apple```

output: Location of "B",```[x,y]```
```python
def sc(apple):
    for x in range(len(apple)):
        for y in range(len(apple[x])):
            if apple[x][y] == 'B':
                return [x,y]
```
```python
def sc(apple):
    return [[x,y.index("B")] for x,y in enumerate(apple) if "B" in y][0]
```
```python
def sc(apple):
    for i in apple :
        for j in i:
            if j == "B" :
                return [apple.index(i),i.index(j)]
```
