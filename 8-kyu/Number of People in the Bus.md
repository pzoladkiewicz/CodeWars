There is a bus moving in the city, and it takes and drop some people in each bus stop.

You are provided a list (or array in JS) of integer array. Each integer array has two items which represent number of people get into bus (The first item) and number of people get off the bus (The second item).

The first integer array has 0 number in the second item, since the bus is empty in the first bus stop.

Your task is to return number of people in the bus after the last bus station. Take a look on the test cases :)

Please keep in mind that the test cases ensure that the number of people in the bus is always >= 0. So the return integer can't be negative.


 for each element in bus_stops list
 add first element and subtract second
```python
def number(bus_stops):
	output = 0
	for el in bus_stops:
		output += el[0] - el[1]
	
	return output
```  

other solutions

```python
def number(bus_stops):
    return sum([stop[0] - stop[1] for stop in bus_stops])
```
```python    
def number(stops):
    return sum(i - o for i, o in stops)
```
