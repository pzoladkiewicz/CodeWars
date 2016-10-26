Deoxyribonucleic acid (DNA) is a chemical found in the nucleus of cells and carries the "instructions" for the development and functioning of living organisms.

If you want to know more [wiki/DNA](http://en.wikipedia.org/wiki/DNA)

In DNA strings, symbols "A" and "T" are complements of each other, as "C" and "G". You have function with one side of the DNA (string, except for Haskell); you need to get the other complementary side. DNA strand is never empty or there is no DNA at all (again, except for Haskell).

> DNA_strand ("ATTGC") # return "TAACG"  
> DNA_strand ("GTAT") # return "CATA"

```
def DNA_strand(dna):
    # code here
    output = ''
    for d in dna:
        if d == 'A':
            output += 'T'
        elif d == 'T':
            output += 'A'
        elif d == 'G':
            output += 'C'
        elif d == 'C':
            output += 'G'
    return output
```

    import string
    def DNA_strand(dna):
        return dna.translate(string.maketrans("ATCG","TAGC"))
        # Python 3.4 solution || you don't need to import anything :)
        # return dna.translate(str.maketrans("ATCG","TAGC"))
  
```  
pairs = {'A':'T','T':'A','C':'G','G':'C'}
def DNA_strand(dna):
    return ''.join([pairs[x] for x in dna])
```

    def DNA_strand(dna):
      return "".join([{'A':'T', 'T':'A', 'C':'G', 'G':'C'}[l] for l in dna])
