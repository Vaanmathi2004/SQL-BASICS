# DATABASE(DB)

* Any collection of related information.
  Ex: Phone Book, Shopping list, Todo list, Your 5 best friends, Facebook's User Base

* Databases can be stored in many ways.
  Ex: On paper, In your mind, On a computer, Powerpoint, Comment section (general database that stores comments of the video)

* Any collection of related information that can be stored in many ways.

Ex: 

Amazon.com vs Shopping list

* Keeps track of Products, Reviews, Purchase Orders, Credit Cards, Users, Media, etc
* Trillions of pieces of information need to be stored and readily available
* Information is extremely valuable and critical to Amazon.com's functioning
* Security is essential, Amazon stores peoples personal information (Credit card #, SSN, Address, phone Information is stored on a computer)
-----
* Keeps track of consumer products that need to be purchased
* 10-20 pieces of information need to be stored and readily available
* Information is for convenience sake only and not necessary for shopping
* Security is not important
* Information is stored on a piece of paper, or even just in someone's memory

        COMPUTERS ARE GREAT AT KEEPING TRACK OF LARGE AMOUNT OF THE INFORMATION

---------------------------------------------------------
**DATABASE MANAGEMENT SYSTEMS(DBMS)**

* Special software program that helps users create and maintain a database on a computer.

  * Makes it easy to manage large amounts of information (Ex: Amazon contains trillions of information)

  * Handle security (People with usernames and password can access the data)

  * Backups

  * Importing / exporting data

  * Concurrency

  * Interacts with software appliations (Programming language)
     Ex: 
      * Amazon.com is a website and it's interacting with amazon databases which is stored most likely using a DBMS.
                         
                AMAZON <--> DBMS
      * Amazon.com will interact with the DBMS in order to create, read, update and delete information.

-------------------------------------------------------

* Database management system is'nt the actual database.  
* DBMS is the software application that is creating, maintaining, updating, deleting information from the actual database.

-------------------------------------------------------

**CRUD**

* Create(creating information in the database/ create new database entries), Read/Retrieve, Update, Delete (existing information)
* It represents the four main operations that we're going to be doing with the database using DBMS.
* Any good DBMS is going to be able to do all four of these operations.

-------------------------------------------------------

**Types of Databases**

1. Relational databases (SQL)
   * Organize data into one or more tables

   * Each table has columns and rows

   * A unique key identifies each rows (Ex: SI.No in table, username in users table)
   (Organize all the data that we want to store by inserting them into predefined tables)

   -------

   **Relational Database Management Systems (RDBMS)**

   * Help users create and maintain a relational database
     Ex: mySQL, Oracle, postgreSQL, mariaDB, etc.

   **Structured Query Language (SQL)**

   * Standardized language for interacting with RDBMS.

   * Used to perform C.R.U.D operations, as well as other administrative tasks (user management, security, backup, etc).

   * Used to define tables and structures

   * SQL code used on one RDBMS is not always portable to another without modification.

   * Create & manage databases. Design & create database tables.

------------

2. Non - relational databases (nosql/ not just sql databases)
   - Organize data in anything but a traditional table

   - Key-value hash (keys are mapped to values)

   - Documents (JSON(Javascript Object Notation), XML, etc)

   - Graphs (Relational nodes there)

   - Flexible Tables
   (Any database that is not relational is referred as non-relational; it's a general category)

  --------

  **Non-Relational Database Management Systems (NRDBMS)**

  - Help users create and maintain a non-relational database

     Ex: mongoDB, dynamoDB, apache cassandra, firebase, etc

  --------

  **Implementation Specific**

  - Any non-relational database falls under this category, so there's no set language standard.

  - Most NRDBMS will implement their own language for performing C.R.U.D and administrative operations on the database.

----------------------------------------------------------

**Database Queries**

* Queries are requests made to the database management system for specific information from the database.

* As the database's structure become more and more complex, it becomes more difficult to get the specific pieces of information we want.
  (If you have a very complex database layout or schema, then getting a specific piece of information can be little bit tricky)
  - That's why we write database queries (complex database = complex database query (like a program))
* Ex: A google search is a query









