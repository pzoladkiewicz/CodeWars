Oh no! Timmys been moved into the database divison of his software company but as we know Timmy loves making mistakes. Help Timmy keep his job by fixing his query...

```sql
SELECT 
  s.transaction_date as day,
  d.name,
  COUNT(s.id)
  FROM department d
    JOIN sale s on d.id = s.id
  group by day, d.name
  order by name desc
```

Timmy works for a statistical analysis company and has been given a task of totaling the amount of sales on a given day grouped by each department and then each day.

#### Resultant table:

* day (type: date)
* department (type: text)
* sale_count (type: int)

```sql
-- for t-sql one can't use alias with GROUP BY
SELECT 
  CAST(s.transaction_date AS date) AS day,
  d.name AS department,
  COUNT(1) AS sale_count
  FROM department d
    JOIN sale s
    ON d.id = s.department_id
  GROUP BY CAST(s.transaction_date AS date), d.name
  ORDER BY day, department
```

Tables and relationship below:

![](https://i.imgur.com/kBkwsbi.png)
