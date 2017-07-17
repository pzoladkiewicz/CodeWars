Given a table of random numbers as follows:

#### numbers table schema
* id
* number1
* number2
* number3
* number4
* number5

Your job is to return a single row table in the following format, where each value is the largest value from its corresponding column:
#### output table schema
* maxnum1
* maxnum2
* maxnum3
* maxnum4
* maxnum5
```sql
SELECT
   MAX(number1) AS maxnum1
	,MAX(number2) AS maxnum2
	,MAX(number3) AS maxnum3
	,MAX(number4) AS maxnum4
	,MAX(number5) AS maxnum5
FROM numbers
```
