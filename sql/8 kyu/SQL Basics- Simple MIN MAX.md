For this challenge you need to create a simple MIN / MAX statement that will return the Minimum and Maximum ages out of all the people.
####people table schema

* id
* name
* age

####select table schema

* age_min (minimum of ages)
* age_max (maximum of ages)
```sql
SELECT min(age) AS age_min, max(age) AS age_max
FROM people
```
