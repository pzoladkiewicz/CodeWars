Bob is preparing to pass IQ test. The most frequent task in this test is ```to find out which one of the given numbers differs from the others```. Bob observed that one number usually differs from the others in evenness. Help Bob — to check his answers, he needs a program that among the given numbers finds one that is different in evenness, and return a position of this number.

```!``` Keep in mind that your task is to help Bob solve a ```real IQ test```, which means indexes of the elements start from ```1 (not 0)```

Examples :
```python
iq_test("2 4 7 8 10") => 3 # Third number is odd, while the rest of the numbers are even

iq_test("1 2 1 1") => 2 # Second number is even, while the rest of the numbers are odd
```
```python
def iq_test(numbers):
    
    nums = [int(n) for n in numbers.split()]
    
    isEven = [int(n) for n in numbers.split() if int(n)%2 == 0]

    if len(isEven) == 1:
        return nums.index(sum(isEven)) + 1 
    else:
        return nums.index(sum([int(n) for n in numbers.split() if int(n)%2 != 0])) + 1
```
```python
def iq_test(numbers):
    e = [int(i) % 2 == 0 for i in numbers.split()]

    return e.index(True) + 1 if e.count(True) == 1 else e.index(False) + 1
```
