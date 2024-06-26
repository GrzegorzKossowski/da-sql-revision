# SQL SELECT Statement

[← README.md](../README.md)

The SELECT statement is used to select data from a database.

The data returned is stored in a result table, called the result-set.

## SELECT Syntax

```sql
SELECT * FROM tablename;
```
---

```sql
SELECT column1, column2, ...
  FROM tablename;
```

Here, column1, column2, ... are the field names of the table you want to select data from. If you want to select all the fields available in the table, use the following syntax:


## SELECT Column Example

The following SQL statement selects the "first_name" and "last_name" columns from the "patients" table:

```sql
SELECT first_name, last_name FROM patients;
```

## SELECT * Example

The following SQL statement selects all the columns from the "patients" table:

```sql
SELECT * FROM patients;
```

[← README.md](../README.md)