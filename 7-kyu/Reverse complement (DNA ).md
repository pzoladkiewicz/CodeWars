In genetic the reverse complement of a sequence is formed by reversing the sequence and then taking the complement of each symbol.

The four nucleotides in DNA is Adenine (A), Cytosine (C), Guanine (G) and Thymine (Thymine).

* A is the complement of T
* C is the complement of G.

This is a bi-directional relation so:

* T is the complement of A
* G is the complement of C.

For this kata you need to complete the reverse complement function that take a DNA string and return the reverse complement string.

Note: You need to take care of lower and upper case. And if a sequence conatains some invalid characters you need to return "Invalid sequence".
```py
def reverse_complement(dna):
    rev = {
           'A':'T',
           'T':'A',
           'C':'G',
           'G':'C'
            }
            
    for d in dna:
        if d.upper() not in 'ATCG':
            return 'Invalid sequence'
                        
    return ''.join(rev[d.upper()] for d in reversed(dna))
```
```py
def reverse_complement(dna):
    rev = {
           'A':'T',
           'T':'A',
           'C':'G',
           'G':'C'
            }
            
    if any(d.upper() not in 'ATCG' for d in dna):
        return 'Invalid sequence'
    else:
        return ''.join(rev[d.upper()] for d in reversed(dna))
```
