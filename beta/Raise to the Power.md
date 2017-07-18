Given the following table 'decimals':
#### decimals table schema
* id
* number1
* number2
Return a table with one column (result) which is the output of number1 raised to the power of number2.
```sql
SELECT
    POWER(number1, number2) AS result
FROM decimals
```
