Create a simple SELECT query to display student information of all ACTIVE students.
####students table structure
* Id
* FirstName
* LastName
* IsActive

Note: IsActive (true or false)
```sql
SELECT   FirstName
        ,LastName
        ,IsActive
FROM students
WHERE IsActive = 1
```
