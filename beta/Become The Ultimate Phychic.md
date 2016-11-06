###Let's play Phychic

(on folks who aren't very good at math)

Given a box containg certain number of balls 'n'. where 0<n<=50. The balls could be either Green, Red, or Blue. A green ball weighs 5kg, A red ball weighs 4kg and A blue ball weighs 3kg. Guess the exact amount of green,red and blue balls in the box(in the form [[green,red,blue]], given the total mass of all balls in the box as 'm'

If there is more than one possibility, then return all possibilities in increasing order of green balls. e.g Given n=3 and m=12, the return should be: [[0,3,0],[1,1,1]]
#####ASSUME ALL INPUTS A LOGICALLY CORRECT
#####DONT TEST FOR ANY INPUT ERROR
   
   
```
def Guess_it(n,m):
  #May the force be with you.
    output = []
  
    for g in range(n+1):
        for r in range(n+1-g):
            for b in range(n+1-g-r):
                if (g+r+b == n) and (g*5 + r*4 + b*3 == m):
                    output.append([g, r, b])
    return output
```

