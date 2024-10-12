 # CONSTRAINTS

 - We can add contraints onto the specific column of the table that can control like what types of information or rows can be put inside of there.
 - It is a advanced way of inserting information into the database.
 
 ## NOT NULL
 - NOT NULL will allow us to define that a particular column in the table cannot be null. (NULL - that represents no value)
 ```SQL
name VARCHAR(20) NOT NULL,
 ```
 - So, if you insert row into the table, you can't insert null as a name.
 - If so, you will get the error message.

 ## UNIQUE
 - It means that the particular column has to be unique for each row in the table.
 ```SQL
major VARCHAR(20) UNIQUE,
 ```
 - If somebody else or another row in the table has the same major as another entry, then that will get rejected.
 - If so, you will get the error message as `Duplicate entry 'Biology' for key 'major'`.

 ```
 PRIMARY KEY IS AN ATTRIBUTE OR A COLUMN ON THE TABLE THAT IS BOTH 'NOT NULL' AND 'UNIQUE'
 ```

## DEFAULT

- If the entry for that column is left blank, we can set the default value for it that we place over.

```SQL
major VARCHAR(20) DEFAULT 'undecided',
```

```SQL
INSERT INTO tablename(student_id, name) VALUES(1, 'JACK')
```
DATABASE:
| student-id|name|major|
|-----------|-----------|-----------|
| 1 | JACK | undecided |  

## AUTO_INCREMENT
- It going to specify that the data that gets inserted into that column is going to automatically incremented everytime we add one in.
- If we didn't specify the value, it starts from 1 and gets incremented for each row.
```SQL
student_id INT AUTO_INCREMENT,
```
```SQL
INSERT INTO tablename(name,major) VALUES( 'JACK', 'Biology'),
INSERT INTO tablename(name,major) VALUES( 'KEN', 'Sociology'),
```
DATABASE:
| student-id|name|major|
|-----------|-----------|-----------|
| 1 | JACK | Biology |
| 2 | KEN | Sociology |  

