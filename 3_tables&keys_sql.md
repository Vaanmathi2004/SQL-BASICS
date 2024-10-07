# TABLES AND KEYS
•	Tables are used to store information in relational databases.

•	Student table defines specific information about the students.

•	All tables in relational database are going to have two things - columns and rows.

1.	Column (vertical section) 
     - Defines the single attribute
     - Column names – student_id, name, major
     - This table is storing three pieces of information about each student.
2.	Row (Horizontal section) 
     - Represents the single student.
     - In single row, we’re storing the students ID, the name and the major.

## KEYS:

1.	Primary Key

     - One special column that we want whenever we create table in relational database.
     - It is an attribute which uniquely defines the row and differentiate the rows in the databases.
     - Primary key can be strings, numbers or anything.
     - Ex: student_id column 
     - The attributes inside this column is the primary key which is used to uniquely identify a specific row.
     - Ex: 

        1.Kate’s primary key is 2.

       2.. Two Jack in both of which is biology majors and can identify each of them with primary key that is unique for each individual.

## TYPES OF PRIMARY KEYS:
1.	**Surrogate key**
     - 	Key that has no mapping to anything in the real world but only in the databases.
     - Ex: emp_id
     - Random number that is assigned to the employee.
     - Number that doesn’t mean anything. It is just used to represent the employee inside the databases.

2.	**Natural key**
     - Key that has a mapping or purpose in the real world, not only in the database.
     - Examples include Aadhar number which is used to uniquely identify each citizen in India, can be used to uniquely identify each citizen’s information in the databases.

3. **Foreign Key**
 
 
    - Attribute that we can store on a database table that will link us to another database table or same database table.
    - Ex: branch_id of the employee table
    - Foreign key stores the primary key of a row of another database table or same database table.
    - Ex: branch_id of the branch table
    - It is just the way to define relationships between the tables or within the table.
    - One particular table can have any number of foreign keys as columns.

Another database table
    - Ex: Jan Levinson of employee table have branch id ‘1’ which means she belongs to ‘corporate’ branch in the branch table.

       Foreign key - branch_id of the employee table
       Primary key - branch_id of the branch table

   - Ex: Branch name ‘Scranton’ have manager id ‘101’ in branch table in which it refers to employee id ‘101’ who is ‘Michael Scott’ in employee table.
(Foreign key – mgr_id of the branch table
  Primary key - emp_id of the branch table)



Same database table

 - Ex: Employee id ‘101’ have supervisor id ‘100’ which refers to the employee id ‘100’. Jan Levinson is the supervisor of Michael Scott.
(Foreign key – super_id of the employee table
Primary key - emp_id of the employee table)

3.	 **Composite key**
 
 - 	Primary key consists of two columns called Composite key.
 -  Key that needs two attributes.
 -  Each attribute is not enough to uniquely identify the row of the databases.
 - Only together, the attributes can uniquely identify the each row.
 - Ex: In branch supplier table, each column has repeated values, in which the composite key is used to uniquely identify each rows (defining two columns as a primary key).
- Both of the emp_id, client_id are foreign keys. Both make the primary key of the table.
