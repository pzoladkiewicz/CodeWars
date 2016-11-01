Write a function, which takes a non-negative integer (seconds) as input and returns the time in a human-readable format (HH:MM:SS)

* ```HH``` = hours, padded to 2 digits, range: 00 - 99
* ```MM``` = minutes, padded to 2 digits, range: 00 - 59
* ```SS``` = seconds, padded to 2 digits, range: 00 - 59

The maximum time never exceeds 359999 (```99:59:59```)

You can find some examples in the test fixtures.


    def make_readable(seconds):
        hrs = seconds // (60*60)
        mins = (seconds - hrs * 60 * 60)// 60
        secs = seconds - mins*60 - hrs * 60 * 60

        return str('{0:02}'.format(hrs)) + ':' + str('{0:02}'.format(mins)) + ':' + str('{0:02}'.format(secs))

```
def make_readable(s):
    return '{:02}:{:02}:{:02}'.format(s / 3600, s / 60 % 60, s % 60)
```
