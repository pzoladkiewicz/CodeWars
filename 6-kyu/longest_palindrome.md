Longest Palindrome

Find the length of the longest substring in the given string s that is the same in reverse.

As an example, if the input was “I like racecars that go fast”, the substring (racecar) length would be 7.

If the length of the input string is 0, return value must be 0.

Example:

    "a" -> 1 
    "aab" -> 2  
    "abcde" -> 1
    "zzbaabcd" -> 4
    "" -> 0
```py
def longest_palindrome (s):

    longest = 0
    length = len(s)
    
    for outer in range(length+1):
        for inner in range(outer, length+1):
            check = s[outer:inner]
            if check == check[::-1] and len(check) > longest:
                longest = len(check)
    return longest
```
