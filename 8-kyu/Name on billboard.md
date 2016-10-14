You can print your name on a billboard ad. Find out how much it will cost you. Each letter has a default price of £30, but that can be different if you are given 2 parameters instead of 1.

You can not use multiplier "*" operator.

If your name would be Jeong-Ho Aristotelis, ad would cost £600. 20 leters * 30 = 600 (Space counts as a letter).

```
def billboard(name, price=None):
    #your code here - note that in Python we cannot prevent the use of the
    #multiplication, but try not to be lame and solve the kata in another way!
    cost = 0
    
    if not price:
        price = 30
    for i in name:
        cost += price
                  
    return cost
```
```
def billboard(name, price=30):
    return sum(price for letter in name)
```
