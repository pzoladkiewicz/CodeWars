Your task is to make a function that can take any non-negative integer as a argument and return it with it's digits in descending order. Descending order means that you take the highest digit and place the next highest digit immediately after it.

Examples:

Input: 145263 Output: 654321
Input: 1254859723 Output: 9875543221

convert to str => str(num)
sort => ''.join(sorted(..)
revese => ..[::-1]
convert to int => int(..)


def Descending_Order(num):
  return int(''.join(sorted(str(num)))[::-1])
    
other solution

def Descending_Order(num):
  return ''.join(sorted(str(num), reverse = True))
