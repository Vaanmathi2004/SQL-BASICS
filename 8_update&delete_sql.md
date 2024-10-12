# UPDATE AND DELETE

## UPDATE
- We can update a specific column or rows or group of it.

### EXAMPLE 1:
```SQL
UPDATE tablename
SET major = 'Bio'
WHERE major = 'Biology';
```
- This statement will update the major column in which wherever it is biology, that will be updated as Bio.
 - We can also update specifically as follows:

### EXAMPLE 2:

 ```SQL
UPDATE tablename
SET major = 'Bio'
WHERE student_id = 4;
```
- student_id '4' 's major will be updated as Bio.

### EXAMPLE 3:

```SQL
UPDATE tablename
SET major = 'Biochemistry'
WHERE major = 'Biology' OR major = 'Chemistry';
```
- Student having Biology major or Chemistry major will be updated as Biochemistry major.
- 'WHERE' statement is used to specifically updating.

### EXAMPLE 4:

```SQL
UPDATE tablename
SET name = 'Tom' , major = 'undecided'
WHERE student_id = 1;
```
- You can change multiple columns within the same query.

### EXAMPLE 5:
```SQL
UPDATE tablename
SET major = 'Bio'
```
- All the rows of the 'major' column will be updated as 'Bio'.

## DELETE

- We can delete a specific column or rows or group of it.

### EXAMPLE 1:

```SQL
DELETE FROM student
```
- This will delete all the rows inside of the table.
- Deletes everything from the table.

### EXAMPLE 2:

```SQL
DELETE FROM student
WHERE student_id = 5;
```
- This will delete any rows from the table having student_id as '5'.

### EXAMPLE 3:

```SQL
DELETE FROM student
WHERE name = 'Tom' AND major = 'undecided';
```
- This will delete any rows from the table having name as 'Tom' and major as 'undecided'.