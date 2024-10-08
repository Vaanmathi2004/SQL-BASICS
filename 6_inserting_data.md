# INSERTING DATA

In order to insert a piece of information into a table (that we set up),
```SQL
INSERT INTO tablename VALUES(1, 'Jack', 'Biology');
```
  - We end each query with semicolon
  - Inside the values paranthesis, we need to enter the data with respect to the columns(attributes) we created while setting up the table.
  - This information will be inserted into the database table.

```SQL
SELECT * FROM student;
```
- This statement will grab and give all the information from the student table
-----------
- If one student didn't have or don't know the data to insert into that attribute of their row.
- We can modify the statement by,

```SQL
INSERT INTO tablename(student_id,name) VALUES(1, 'Jack');
```
- Inside the tablename paranthesis, we specify the name of the attributes to which we are going to insert the data.
- With respect to attributes inside tablename paranthesis, we enter data inside values paranthesis.
- So while displaying the table, attribute's value(that we didn't inserted) will be displayed as `NULL`.
---------------
- As we mentioned student_id as primary key, if we insert duplicate value into it, it will show error as `Duplicate entry '3' for key 'PRIMARY' `   (3 is a duplicate student_id).
 