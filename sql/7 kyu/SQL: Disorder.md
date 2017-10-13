You are given a table ```numbers``` with just one column, ```number```. It holds some numbers that are already ordered.

You need to write a query that makes them un-ordered.
```sql
SELECT *
FROM numbers
ORDER BY random()
```
