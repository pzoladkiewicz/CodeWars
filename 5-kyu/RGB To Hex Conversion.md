The rgb() method is incomplete. Complete the method so that passing in RGB decimal values will result in a hexadecimal representation being returned. The valid decimal values for RGB are 0 - 255. Any (r,g,b) argument values that fall out of that range should be rounded to the closest valid value.

The following are examples of expected output values:
```
rgb(255, 255, 255) # returns FFFFFF
rgb(255, 255, 300) # returns FFFFFF
rgb(0,0,0) # returns 000000
rgb(148, 0, 211) # returns 9400D3
```
```python
    def rgb(r, g, b):
        output = ''
        r = 0 if r < 0 else r
        g = 0 if g < 0 else g
        b = 0 if b < 0 else b
        r = 255 if r > 255 else r
        g = 255 if g > 255 else g
        b = 255 if b > 255 else b

        output += '{0:02X}'.format(r)
        output += '{0:02X}'.format(g)
        output += '{0:02X}'.format(b)
        return output
```
