In the following 6 digit number:

283910
91 is the greatest sequence of 2 digits.

Complete the solution so that it returns the largest five digit number found within the number given.. The number will be passed in as a string of only digits. It should return a five digit integer. The number passed may be as large as 1000 digits.

Adapted from ProjectEuler.net
_____________________________
```py
def solution(digits):
	
    # iterate over digits and for each 5 number digit check if its larger than max
    # if so new max is equal to currently checked number
    
    max = 0
    for number in range(len(digits)-4):
		temp = int(digits[number:number+5])
		if temp > max:
			max = temp
            
    return max
```
```py
def solution(dd):
    return max(int(dd[i:i+5]) for i in range(len(dd) - 4))
```
