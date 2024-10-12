- Query is a block of SQL that's designed to ask the DBMS for a particular piece of information.

## SELECT
- It is a keyword that tells the RDBMS that we want to get some information from it.
### EXAMPLE 1
```SQL
SELECT *
```
- This statement will grab all the information from DBMS.
### EXAMPLE 2
```SQL
SELECT * FROM student;
```
- This statement will grab all the columns of information from tablename called student.
### EXAMPLE 3
```SQL
SELECT name FROM student;
```
```SQL
SELECT name, major FROM student;
```
- We can select the specific columns of information that we want to get back from the DBMS.
### EXAMPLE 4
```SQL
SELECT student.name, student.major FROM student;
```
- We can also pre-pen the column name with tablename.columnname
- So it's clear that from which table the column is from.
### EXAMPLE 5

##### EXAMPLE 1
```SQL
SELECT student.name, student.major FROM student
ORDER BY name;
```
- Using `ORDER BY`, we can specify the column to get the alphabetically ordered information.
- Here the 'name' column will be alphabetically ordered and along with the other column in it's rows that remains with it.
- By default, it will be ascending order.

|name|major|
|----------|-----|
|Clarie|Chemsitry|
|Jack|Biology|
|Kate|Sociology|
|Mike|Computer science|

##### EXAMPLE 2

- If we want it in descending order, we use`DESC`.

```SQL
SELECT student.name, student.major FROM student
ORDER BY name DESC;
```
- If we want it in ascending order, we use`ASC`.

##### EXAMPLE 3
```SQL
SELECT *
FROM student
ORDER BY major, student_id;
```
- This will first order the table based on 'major'. Then, if students are having same major, that will be further ordered by 'student_id'.
```SQL
SELECT *
FROM student
ORDER BY major, student_id DESC;
```

### EXAMPLE 6
- We can limit the amount(rows) of results we're getting by `LIMIT`.
```SQL
SELECT *
FROM student
LIMIT 2;
```

```SQL
SELECT *
FROM student
ORDER BY student_id
LIMIT 2;
```
### EXAMPLE 7
```SQL
SELECT *
FROM student
WHERE name IN ('Clarie','Kate','Mike');
```
- If the name is three of those mentioned that in the table's column, it will give back the information about it to us.
## BASICS

- `--` used for comment
### COMPARISON OPERATORS
- `=`equal to
- `<`less than
- `>` greater than
- `<=` less than or equal to
- `>=` greater than or equal to
- `<>` not equal to
- `AND`
- `OR`


