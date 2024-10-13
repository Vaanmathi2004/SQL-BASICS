# NESTED QUERIES
- It's basically a query where we're going to be using multiple select statements in order to get a specific piece of information.
- We're going to need to use the results of one `SELECT` statement
to inform the results of another `SELECT` statement.

### EXAMPLE 1
**PROBLEM** - Find the name of all employees who have sold over 30,000 to a single client.

TABLE 1: Employee table having emp_id, first_name, last_name.
TABLE 2: Works_with table having emp_id,client_id,total_sales.

**SOLUTION**
```SQL
SELECT employee.first_name, employee.last_name
FROM employee
WHERE employee.emp_id IN(
    SELECT works_with.emp_id
    FROM works_with
    WHERE total_sales > 30000
);
```
**RESULT**
|first_name|last_name|
|--|--|
|Michael|Scott|
|Stanley|Hudson|

### EXAMPLE 2
**PROBLEM** - Find all the clients who are handled by the branch that Micheal Scott manages

**SOLUTION**
```SQL
SELECT client.client_name
FROM client
WHERE client.branch_id = ( SELECT employee.branch_id
FROM employee
WHERE first_name = 'Micheal' AND second_name = 'Scott'
);
```
