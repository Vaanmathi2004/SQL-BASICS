### AS
```SQL
SELECT first_name AS forename, last_name AS surname
FROM employee;
```
- It will return the first name and last name from the employee table but column name as forename, surname.

### DISTINCT

```SQL
SELECT DISTINCT gender
FROM employee;
```
- It will return the different genders present in the table"s gender column.

|gender|
|------|
|M|
|F|
