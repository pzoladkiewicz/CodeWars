For those of us who are not very familiar with Python, let's handle the very basic challenge of creating a class named Python. We want to give our Pythons a name, so it should take a name argument that we can retrieve later.

For example:
```python
bubba = Python('Bubba')
bubba.name # should return 'Bubba'
```
```python
class Python():
    def __init__(self, name):
        self.name = name
        
    def name(self):
        return self.name()
```

```
You don't need the name function, as it's never being called.
It looks for the object property 'name', but never calls Python.name().
The act of setting the instance variable is sufficient.
```
```python
class Python():
    def __init__(self, name):
        self.name = name
```
