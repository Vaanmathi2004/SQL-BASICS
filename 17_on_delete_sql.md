# ON DELETE
- Deleting entries in the database when they have foreign keys associated to them.
- In company database, we have complex database schema. We have all sorts of foreign keys that are linking between all sorts of tables.
- It's extremely  useful when we're defining foreign key relationships between tables.

`1.ON DELETE SET
NULL` 

`2. ON DELETE CASCADE`

## ON DELETE SET NULL
- If we delete  employee from employee table that have foreign key(mgr_id), the branch table having mgr_id which is associated with that employee is set to `NULL`.


```SQL
CREATE TABLE branch(
    branch_id INT PRIMARY KEY,
    branch_name VARCHAR(40),
    mgr_id INT,
    mgr_start_date DATE,
    FOREIGN KEY(mgr_id) REFERENCES employee(emp_id) ON DELETE SET NULL 
);

DELETE FROM employee
WHERE emp_id= 102;

SELECT * FROM branch;
```
```SQL
FOREIGN KEY(mgr_id) REFERENCES employee(emp_id) ON DELETE SET NULL
--  This statement denotes that if the employee ID in the employee table gets deleted, I want to set the manager ID equal to `NULL`.
``` 
**BRANCH TABLE** 

|branch_id|branch_name|mgr_id|
|--|---|--|
|1|Corporate|100|
|2|Scranton|NULL| 
|3|Stamford|103|
- It's ok for us to set NULL because mgr_id on the branch table is just a foreign key

**EMPLOYEEE TABLE**

|emp_id|first_name|last_name|birth_day|gender|salary|super_id|
|--|--|--|--|--|--|--|
|100|David|Wallace|1967-11-17|M|250000|NULL|

## ON DELETE CASCADE
- If we delete the employee of employee table whose ID is stored in the manager id column in branch table, then we delete the entire row of branch table in the database.


```SQL
CREATE TABLE branch_supplier(
    branch_id INT,
    supplier_name VARCHAR(40),
    supply_type VARCHAR(40),
    PRIMARY KEY (branch_id, supplier_name),
    FOREIGN KEY(branch_id) REFERENCES branch(branch_id) ON DELETE CASCADE 
);

DELETE FROM branch
WHERE branch_id= 2;

SELECT * FROM branch_supplier;
```

|branch_id|supplier_name|supply_type|
|--|--|--|
|3|Hammer Mill|Paper|
|3|Patriot Paper|Paper|
- There's no longer any branch ID 2 in here.
-----

- branch_id which is a foreign key is also part of primary key
- So the branch_id in the branch supplier table is absolutely crucial for this row in the database.
- If the branch disappears, we can't set branch_id to `NULL` because primary key can't have a `NULL` value. So we have to delete the entire thing otherwise we're going to run into trouble.
- That's why we use `ON DELETE CASCADE` as opposed to `ON DELETE SET NULL`.
