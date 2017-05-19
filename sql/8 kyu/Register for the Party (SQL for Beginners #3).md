You recieved an invitation to an amazing party. Now you need to write an insert statement to add yourself to the table of participants.

participants table schema
```
name (string)
age (integer)
attending (boolean)
```
### NOTES:

Since alcohol will be served, you can only attend if you are 21 or older
You can't attend if the attending column returns anything but true
Don't remove the 'SELECT' command from the solution!
Your solution should use pure SQL. Ruby is used within the test cases to do the actual testing.
```sql
INSERT INTO participants(name, age, attending)
VALUES ('name', 33, true);

SELECT * FROM participants;
```
