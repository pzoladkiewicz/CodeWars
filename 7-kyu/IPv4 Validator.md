In this kata you have to write a method to verify the validity of IPv4 addresses.

*Example of valid inputs:*

"1.1.1.1"

"127.0.0.1"

"255.255.255.255"

*Example of invalid input:*

"1444.23.9"

"153.500.234.444"

"-12.344.43.11"
```py
def ipValidator(ip):
    ip = [i for i in ip.split('.')]
    if len(ip) != 4:
        return False
    else:
        return all(False if not i.isnumeric() or 0 < int(i) > 255 else True for i in ip)
```
```py
from ipaddress import ip_address
def ipValidator(address):
    try:
        ip_address(address)
        return True
    except ValueError:
        return False
# if you use python2 (and get AddressValueError) - convert input address to u"address" (peck_wtf)*
```
