# WILDCARDS
- It is a way of defining different patterns that we want to match specific pieces of data to.
- Grabbing data that matches a specific pattern.

## LIKE
- `Like` is a special SQL keyword which we're going to use with wildcards.
- It is a SQL operator used to compare a pattern in a string.
#### EXAMPLE 1
```SQL
SELECT *
FROM client
WHERE client_name LIKE '%LLC';
-- Returns any client's (row) who are an LLC
-- `WHERE` clause filters rows based on a condition.
```
- Inside the `LIKE` quotation, we're going to define the pattern that can be used by the database in order to find what we need.
- Insdie the quotation, we can use two special characters.
  1. `%` -  any number of characters.
  2. `_` - one character

#### EXAMPLE 2
```SQL
SELECT *
FROM branch_supplier
WHERE supplier_name LIKE '%Label%'
```

#### EXAMPLE 3
```SQL
SELECT *
FROM employee
WHERE birth_date LIKE '____-10%'
-- 4 hypens represents any four characters (Here year)
-- % represents any sequence of characters (Here date)
```
- It will return the employees born in October regardless of year or specific date.

---
- Those will be helpful to search the database for specific information.
- Helpful in searching application