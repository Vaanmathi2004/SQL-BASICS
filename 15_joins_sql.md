# JOINS
- Joins are used to combine rows from two or more tables based on a related column between them.
- It will be useful for combining information from different tables into a single result.

```SQL
SELECT employee.emp_id, employee.first_name, branch.branch_name 
-- As we're joining the branch table, we can use branch.branch_name in select
FROM employee
JOIN branch
ON employee.emp_id= branch.mgr_id;
-- id's of employees are the related column (mgr is also employee)
```
- It's going to join branch table with employee table on the `specific column`.
- `ON employee.emp_id= branch.mgr_id` - we're going to combine the rows of employee table and rows of branch table as long as the emp_id is equal to mgr_id.

|emp_id|first_name|branch_name|
|--|--|--|
|100|David|Corporate|
|102|Michael|Scranton|
- It says that the manager of corporate branch is david having mgr_id & emp_id as 100.
- It only included employees who are branch managers.

## TYPES OF JOINS

- There are `FOUR` types of joins.
1. **INNER JOIN**
   - It will combine two tables whenever they have shared column in common. 
   - Above example.
   - It is a general join type.
2. **LEFT JOIN**
```SQL
SELECT employee.emp_id, employee.first_name, branch.branch_name 
FROM employee
LEFT JOIN branch
ON employee.emp_id= branch.mgr_id;
```
- The left table is the one added from `from` statement.
- With `LEFT JOIN`, we include all of the rows from the left table
- It includes all the rows from employee table along with employees who are the branch managers(`ON` statement).
3. **RIGHT JOIN**
```SQL
SELECT employee.emp_id, employee.first_name, branch.branch_name 
FROM employee
RIGHT JOIN branch
ON employee.emp_id= branch.mgr_id;
```
- The right table is the one included in the `RIGHT JOIN` statement.
- With `RIGHT JOIN`, we include all of the rows from the right table
- It includes all the rows from branch table along with employees who are the branch managers.
----
- `NULL`  will be in results for columns not having values.
4. **FULL OUTER JOIN**
- We can't do it in MySQL.
- It's a `LEFT JOIN` and `RIGHT JOIN` combined.




