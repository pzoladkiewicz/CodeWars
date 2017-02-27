Write a method ```alternate_sq_sum``` (JS: alternateSqSum ) that takes an array of Integers as Input and finds the sum of squares of the elements at even positions (i.e 2nd 4th 6th etc etc elements) and the rest of the elements at odd Position (i.e 1st 3rd etc elements) without squaring them (the odd ones) thus completing whole array.

> NOTE:

> Elements at EVEN POSITION need to be squared, like element at index ( assuming starting index of an array in language to be 0 ) 1,3,5,7.. etc because 1st elements will be at 1st position (though it would have 0 as its index).   

*For Example:*   
```alternate_sq_sum([11, 12, 13, 14, 15]) #should return 379```

*Explanation:*   
elements at indices 0, 2, 4 are 11, 13, 15 and they are at odd positions as 11 is at position #1, 13 is at position #3 and 15 at #5.
elements at indices 1, 3 are 12 and 14 and they are at even position. So we need to add 11, 13, 15 as they are and square of 12 and 14

--> 11 + 13 + 15 + 12^2 + 14^2   
= 11 + 13 + 15 + 144 + 196   
= 379   
```python
def alternate_sq_sum(arr):
    return sum(n**2 if n%2 == 0 else n for n in arr)
```
