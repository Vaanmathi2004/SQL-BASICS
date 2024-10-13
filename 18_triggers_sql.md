# TRIGGERS
- It is a block of SQL code which we can write which will define a certain action that should happen when a certain operation gets performed on the database.

- We can to define triggers in the command line.

- Because we have to change the SQL delimiter that we're going to use.

`MySQL command line client`
- We can open in popsql itself using :
`
mysql -u root -p
`
- It will prompt us to enter the password to login to mclc.

`mysql> use databasename`

- In popsql, we are write trigger code as it will be easier to see.

### EXAMPLE 1
```SQL
DELIMITER $$
CREATE 
    TRIGGER my_trigger BEFORE INSERT
    ON employee
    FOR EACH ROW BEGIN
       INSERT INTO trigger_test VALUES('added new employee');
    END$$
DELIMITER;
```
```SQL 
CREATE 
    TRIGGER my_trigger 
    -- created a trigger named my_trigger
```
- Those deimiter can't be configured on popsql. Delimiter are defined on text editor level.
- In mclc:

`mysql> DELIMITER $$`

`mysql> CREATE  TRIGGER my_trigger BEFORE INSERT ON employee FOR EACH ROW BEGIN  INSERT INTO trigger_test VALUES('added new employee'); END$$`

`mysql> DELIMITER;`

```SQL
INSERT INTO employee
VALUES (109, 'Oscar', 'Martinez', '1968-02-19', 'M', 69000, 106, 3);

SELECT * FROM trigger_test;
```
**OUTPUT**

`added new employee`

```SQL 
CREATE 
    TRIGGER my_trigger 
    -- created a trigger named my_trigger
```
- Before anything new inserted on the employee table, for each of the new item that is getting inserted, i want to insert into the trigger test table , the values 'added new employee'.
- This will be helpful as it automates things.
- We can automate on backend of the database.

### DELIMITER
- It is a special keyword in MySQL.
- It will change the MySQl delimiter. Normally the MySQL delimiter is a semicolon.
- It delimits the different SQL command.
- As I'm using `('added new employee');` semicolon here to end off the SQL command here, I can't actually use that same delimiter in order to end off the trigger creation.
- If I did, I'm saying that I'm ending off the trigger, which clearly is not.
- So, I'm changing the delimiter to `$$`. `END$$` says that the trigger is done being created.
- And We can just change the delimiter back to semicolon `DELIMITER;`

### EXAMPLE 2
```SQL
DELIMITER $$
CREATE 
    TRIGGER my_trigger BEFORE INSERT
    ON employee
    FOR EACH ROW BEGIN
       INSERT INTO trigger_test VALUES(NEW.first_name);
    END$$
DELIMITER;
```
- `NEW.first_name` - It's actually allowing us to access a particular attribute about the thing that we just inserted.
- `NEW` refers to the row that we inserted, `.first_name` - I can access specific columns(here first_name) from that row.
- `NEW.first_name` will allow us to get the first name of the employee that's getting inserted.
```SQL
INSERT INTO employee
VALUES (109, 'Oscar', 'Martinez', '1968-02-19', 'M', 69000, 106, 3);

SELECT * FROM trigger_test;
```
**OUTPUT**
added new employee
Kevin

```SQL
DELIMITER $$
CREATE
   TRIGGER my_trigger2 BEFORE INSERT
   ON employee
   FOR EACH ROW BEGIN
      IF NEW.gender = 'M' THEN
        INSERT INTO trigger_table VALUES('added male employee');
      ELSEIF NEW.gender = 'F' THEN
        INSERT INTO trigger_table VALUES('added female employee');
      ELSE 
        INSERT INTO trigger_table VALUES('added other employee');
      END IF;
    END $$
DELIMITER ;
```
- In this trigger, we are using condition.

```SQL
INSERT INTO employee
VALUES (109, 'Ella', 'Martinez', '1968-02-19', 'F', 69000, 106, 3);

SELECT * FROM trigger_test;
```
**OUPUT**

`added female`
----
- Here, we created trigger for `INSERT`, we can also create trigger for `INSERT`, `UPDATE`, `DELETE`.
- We can also do `AFTER INSERT`. Here we wrote as `BEFORE INSERT`.

- In mclc:
`mysql > DROP TRIGGER my_trigger`
- So the `my_trigger` will no longer be active.