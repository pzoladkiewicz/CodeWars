You are a border guard sitting on the Canadian border. You were given a list of travelers who have arrived at your gate today. You know that American, Mexican, and Canadian citizens don't need visas, so they can just continue their trips. You don't need to check their passports for visas! You only need to check the passports of citizens of all other countries!

Select names, and countries of origin of all the travelers, excluding anyone from Canada, Mexico, or The US.

travelers table schema
* name
* country    
NOTE: The United States is written as 'USA' in the table.
```sql
SELECT
    *
FROM
    travelers
WHERE 1=1
    AND country NOT IN ('USA', 'Mexico', 'Canada')
```
