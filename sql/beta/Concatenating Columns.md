Given the table below:
#### names table schema
id
prefix
first
last
suffix

Your task is to return a sinlge column table containing the full title of the person (concatenate all columns together), as follows:
#### output table schema
title

Don't forget to add spaces.
```sql
SELECT
  CONCAT(prefix, ' ', first, ' ', last, ' ', suffix) AS title
FROM names
```
