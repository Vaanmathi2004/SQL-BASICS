# SQL BASICS
* Structured Query Language (SQL)
* SQL is a language used for interacting with Relational Database Management Systems (RDBMS)
* You can use SQL to get the RDBMS to do things for you
* Create, retrieve, update & delete data
* Create & manage databases
* Design & create database tables
* Perform administration tasks (security, user management, import/export, etc)

-----------

* SQL implementations vary between systems
* Not all RDBMS' follow the SQL standard to a 'T'
* The concepts are the same but the implementation may vary

-----------

* SQL is actually a hybrid language, it's basically 4 types of languages in one

1. **Data Query Language (DQL)**
     - Used to query the database for information.
     - Get information that is already stored there

2. **Data Definition Language (DDL)**
     - Used for defining database schemas.

3. **Data Control Language (DCL)**
     - Used for controlling access to the data in the database.
     - User & permissions management

4. **Data Manipulation Language (DML)**
     - Used for inserting, updating and deleting data from the database.

## Queries

-  A query is a set of instructions given to the RDBMS (written is SQL) that tell the RDBMS what information you want it to retrieve for you
- TONS of data in a DB
- Often hidden in a complex schema
- Goal is to only get the data you need

```SQL
SELECT employee.name, employee.age

FROM employee

WHERE employee.salary > 30000;
```