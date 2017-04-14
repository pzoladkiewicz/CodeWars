When provided with a letter, return its position in the alphabet.

Input :: "a"

Ouput :: "Position of alphabet: 1"

```python
import string
def position(alphabet):
    return 'Position of alphabet: ' + str(string.ascii_lowercase.index(alphabet)+1)
```
