Create a function that returns the sum of the two lowest positive numbers given an array of minimum 4 integers. No floats or empty arrays will be passed.

For example, when an array is passed like [19,5,42,2,77], the output should be 7.

[10,343445353,3453445,3453545353453] should return 3453455.

Hint: Do not modify the original array.

    def sum_two_smallest_numbers(numbers):
        temp = numbers[:]

        m1 = min(temp)
        temp.remove(m1)
        m2 = min(temp)

        return m1 + m2
        
```
def sum_two_smallest_numbers(numbers):
    return sum(sorted(numbers)[:2])
```

    def sum_two_smallest_numbers(num_list):
        num_list.sort()
        return num_list[0] + num_list[1]
