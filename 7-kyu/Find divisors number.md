Find the number of divisors of a positive integer n.

Example:

      divisors(4) -> 3 -- 1, 2, 4
      divisors(5) -> 2 -- 1, 5
      divisors(12) -> 6 -- 1, 2, 3, 4, 6, 12
      divisors(30) -> 8 -- 1, 2, 3, 5, 6, 10, 15, 30
```     
def divisors(n):
    x = 0
    for i in range(1, n+1):
        if n%i == 0:
            x += 1
    return x
```

          def divisors(n):
              return  len([l_div for l_div in range(1, n + 1) if n % l_div == 0]);
```
      def divisors(n):
          return sum(1 for i in xrange(1, n + 1) if n % i == 0)
```
