# UNION
- Union is a special SQL operator which we can use to combine the results of multiple select statements into one.
```SQL
SELECT first_name
FROM employee
UNION
SELECT branch_name
FROM branch;
```
- It lists employees and branch names in the single column with column name is first select statement's column name by default.
### Rules for union
1. first rule is that in all the select statement, there should be equal number of columns that are queries from the respective table, if not error will occur.
2. Second rule is that all the select statement's column should be of similar datatype, so we're able to return it in same result.
- If two columns are queried on all the select statements, the result also jreturn two columns.
```SQL
SELECT first_name
FROM employee
UNION
SELECT branch_name
FROM branch
UNION
SELECT client_name
FROM client;
```

```SQL
SELECT first_name AS company_Names
FROM employee
UNION
SELECT branch_name
FROM branch
UNION
SELECT client_name
FROM client;
-- 'AS' used for result column's name
```
```SQL
SELECT first_name, employee.brand_id
FROM employee
UNION
SELECT branch_name
FROM branch
UNION
SELECT client_name, client.brand_id
FROM client;
-- as similar column name from both the select, tablename.columnname makes it more readable and avoids any circumstances
```
