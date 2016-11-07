####Permutation position

In this kata you will have to permutate through a string of lowercase letters, each permutation will start at a and you must calculate how many iterations it takes to reach the current permutation.

_examples:_

    input: 'a'
    result: 1

    input: 'c'
    result: 3

    input: 'z'
    result: 26

    input: 'foo'
    result: 3759

    input: 'aba'
    result: 27

    input: 'abb'
    result: 28
    
```
def permutation_position(perm):
    alfa = "abcdefghijklmnopqrstuvwxyz"
    text = perm[::-1] #reverse text
    output = 0
    
    for l in range(len(text)):
        letterPosition = alfa.index(text[l])
        output += (len(alfa)**l)*letterPosition

    return output + (1 if len(perm) > 0 else 0)
```
