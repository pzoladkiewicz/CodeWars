For this kata we will be using the [DVD Rental database](http://www.postgresqltutorial.com/postgresql-sample-database/).

Your are working for a company that wants to reward its top 10 customers with a free gift. You have been asked to generate a simple report that returns the top 10 customers by total amount spent. Total number of payments has also been requested.

The query should output the following columns:

* customer_id [int4]
* email [varchar]
* payments_count [int]
* total_amount [float]

and has the following requirements:

> only returns the 10 top customers, ordered by total amount spent

```sql
SELECT c.customer_id
        , c.email
        , COUNT(p.payment_id) AS payments_count
        , CAST(SUM(p.amount) AS float) AS total_amount
FROM customer AS c
JOIN payment AS p
ON p.customer_id = c.customer_id
GROUP BY c.customer_id

ORDER BY total_amount DESC
LIMIT 10
```
####Database Schema
![Database Schema](http://www.postgresqltutorial.com/wp-content/uploads/2013/05/PostgreSQL-Sample-Database.png)
