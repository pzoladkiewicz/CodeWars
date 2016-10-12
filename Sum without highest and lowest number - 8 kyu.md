Sum all the numbers of the array except the highest and the lowest element (the value, not the index!).
(Only one element at each edge, even if there are more than one with the same value!)

Example:

    { 6, 2, 1, 8, 10 } => 16
    { 1, 1, 11, 2, 3 } => 6


If array is empty, null or None, or if only 1 Element exists, return 0.
Note: in C++ instead null an empty vector is used. 

    def sum_array(arr):
        if arr:
            return sum(sorted(arr)[1:-1])
        else:
            return 0
.

    def sum_array(arr):
        return sum(sorted(arr)[1:-1]) if arr else 0
