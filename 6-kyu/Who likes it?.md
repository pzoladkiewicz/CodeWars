You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.

Implement a function ```likes :: [String] -> String```, which must take in input array, containing the names of people who like an item. It must return the display text as shown in the examples:

    likes [] // must be "no one likes this"
    likes ["Peter"] // must be "Peter likes this"
    likes ["Jacob", "Alex"] // must be "Jacob and Alex like this"
    likes ["Max", "John", "Mark"] // must be "Max, John and Mark like this"
    likes ["Alex", "Jacob", "Mark", "Max"] // must be "Alex, Jacob and 2 others like this"
For more than 4 names, the number in ``and 2 others``` simply increases.

    def likes(names):
      namesLen = len(names)
      if namesLen == 0:
        return str('no one likes this')
      elif namesLen == 1:
        return str(names[0] + ' likes this')
      elif namesLen == 2:
        return str(names[0] + ' and ' + names[1] + ' like this' )
      elif namesLen == 3:
        return str(names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this' )
      else:
        return str(names[0] + ', ' + names[1] + ' and ' + str(namesLen - 2)  + ' others like this' )
        
```
def likes(names):
    n = len(names)
    return {
        0: 'no one likes this',
        1: '{} likes this', 
        2: '{} and {} like this', 
        3: '{}, {} and {} like this', 
        4: '{}, {} and {others} others like this'
    }[min(4, n)].format(*names[:3], others=n-2)
```

    def likes(names):
        formats = {
                0: "no one likes this",
                1: "{} likes this",
                2: "{} and {} like this",
                3: "{}, {} and {} like this",
                4: "{}, {} and {others} others like this"
            }
        n = len(names)
        return formats[min(n,4)].format(*names, others=n-2)

```
def likes(names):
    if len(names) == 0:
        return "no one likes this"
    elif len(names) == 1:
        return "%s likes this" % names[0]
    elif len(names) == 2:
        return "%s and %s like this" % (names[0], names[1])
    elif len(names) == 3:
        return "%s, %s and %s like this" % (names[0], names[1], names[2])
    else:
        return "%s, %s and %s others like this" % (names[0], names[1], len(names)-2)
```
