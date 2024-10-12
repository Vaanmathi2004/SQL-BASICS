# FUNCTIONS

## COUNT
#### EXAMPLE 1
```SQL
SELECT COUNT(emp_id)
FROM employee;
-- It will return the number of employee id in the employee table that have values (Not null)
```
- `COUNT` is a special SQL function.

|COUNT(emp_id)|
|--|
|9|
#### EXAMPLE 2
```SQL
SELECT COUNT(emp_id)
FROM employee
WHERE gender = 'F' AND birth_date > '1970-01-01';
```
- It will return the number of female employees born after 1970.

## AVG
#### EXAMPLE 1

```SQL
SELECT AVG(salary)
FROM employee;
```
- It will return the average of all employee's salaries.

|AVG(salary)|
|--|
|92888.8889|

#### EXAMPLE 2
```SQL
SELECT AVG(salary)
FROM employee
WHERE gender = 'F';
```
- It will return the average of all female employee's salaries.

## SUM
```SQL
SELECT SUM(salary)
FROM employee;
```
- It will return the sum of all employee's salaries.
-----
### GROUP BY
- Using aggregation in order to organize the data that we get from using these functions.
#### EXAMPLE 1
```SQL
SELECT COUNT(gender), gender 
FROM employee
GROUP BY gender;
```
- It will return the number of males and females in employee table.

|COUNT(gender)|gender|
|--|--|
|3|F|
|6|M|

#### EXAMPLE 2
```SQL
SELECT SUM(total_sales), emp_id
FROM works_with
GROUP BY emp_id;
```
- It will return total sales of each salesman.