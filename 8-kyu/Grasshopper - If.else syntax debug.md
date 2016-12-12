While making a game, your partner, Greg, decided to create a function to check if the user is still alive called ```checkAlive```. Unfortunately, Greg made some errors while creating the function.

```checkAlive``` should return true if the player's health is greater than 0 or false if it is 0 or below.

```checkAlive``` receives one parameter health which will always be a whole number between -10 and 10.
```py
def checkAlive(health):
    return True if health > 0 else False
```
```py
def checkAlive(health):
    return health > 0
```
