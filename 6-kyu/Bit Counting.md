Write a function that takes an (unsigned) integer as input, and returns the number of bits that are equal to one in the binary representation of that number.

Example: The binary representation of ```1234``` is ```10011010010```, so the function should return ```5``` in this case

    def countBits(n):
        output = 0
        for x in bin(n)[2:]:
            output += int(x)
        return output
        
```
def countBits(n):
    return bin(n).count("1")
```

    def countBits(n):
        return sum(int(x) for x in bin(n)[2:])    
