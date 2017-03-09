n investing, one way of determining where a stock is a worthwhile buy is by comparing a stock's current price to a stock's price at its all time high.

If a stock's current price is less than or equal to 80% of its all time high, then it's a "buy".

Build a buy calculator takes the current price of a stock, and the stock's all time high, and returns "Buy" if the stock is a buy, or "Pass" if it's not worthwhile. 
```python
def buy_or_pass(stock_price, all_time_high):
    return 'Buy' if stock_price <= all_time_high * .8 else 'Pass'        
```
