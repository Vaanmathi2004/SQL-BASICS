## CREATING TABLES

**BEFORE THAT**

1. mysql server
```
sql > create database db_name;
```

2. popsql (Text editor where we can write our sql code)
   1. Create connection with mysql
   2. username as root
   3. Save and test
   4. Connect
   5. Write query and run
   6. SQL query will be automatically run on mysql server

## DATATYPES

The basic datatypes used in SQL are,  
(Based on RDBMS, different datatypes to do different things )

| SI.NO|Datatype|Explanation|
|-----------|-----------|-----------|
|1|INT|whole numbers|
|2|DECIMAL(M,N)|Decimal numbers    (M-total no of digits for number, N- no of digits that occurs after the decimal point) Exact values|
|3|VARCHAR(l)|Ex: DECIMAL(3,2) - 4.25 - Variable characters - String of text of length 1|
|4|BLOB|Binary large object, Structure that stores large amount of binary data Ex: can store images, files inside BLOB|
|5|DATE|YYYY-MM-DD|
|6|TIMESTAMP |'YYYY-MM-DD HH:MM:SS' -used for recording like when the item got inserted into the database.|
_____________________________________________________________________________

### DEFINING THE DATABASE SCHEMA

* Whenever you're working with RDBMS, your 1st step is to create tables by 
defining the table layout using SQL command with passsing the attributes(columns) inside it.

________________________________________________________________________________

### CREATING THE TABLE
```SQL
CREATE TABLE student
```
 - student - table name 
 -  CAPS - Sequel reserved words, just the convention that differentiates sql from other text not compulsory
 ```SQL
    student_id INT PRIMARY KEY, name VARCHAR(20), major VACHAR(20);
```
  - INT - type of data you want to store in this column 'student_id' 
  - This column is defined as primary key
  - To have mindfulness in length as that gonna take up a lot of extra space in your database for each row
    

Or Primary key can be defined like this too:

```SQL
CREATE TABLE student (
    student_id INT ,
    name VARCHAR(20),  
    major VACHAR(20),
    PRIMARY KEY(student_id)
); 
```


___________________________________________________________________________________

```SQL
DESCRIBE student; 
```
  - describes the table we created
  - If the table is not created or deleted, 
                     error will be - ``ER_NO_SUCH_TABLE : Table 'db_name.table_name' doesn't exsit``              
____________________________________________________________________________

**DELETE AND MODIFY THE TABLE**
* DELETE:

```SQL
DROP TABLE student;
```


* MODIFY:

  1. ADDING ANOTHER COLUMN:

    ```SQL
      ALTER TABLE student ADD gpa DECIMAL(3,2);
    ```

  2. DELETING THE COLUMN:

    ```SQL
    ALTER TABLE student DROP COLUMN gpa;
    ```




