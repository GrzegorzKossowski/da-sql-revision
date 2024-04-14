# SQL SELECT DISTINCT Statement

[← README.md](../README.md)

The SELECT DISTINCT statement is used to return only distinct (different) values.

Inside a table, a column often contains many duplicate values; and sometimes you only want to list the different (distinct) values.

## SELECT DISTINCT Syntax

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

## SELECT Example Without DISTINCT

The following SQL statement selects all (including the duplicates) values from the first_name column in the patients table:

```sql
SELECT first_name
FROM patients;
```

Now, let us use the SELECT DISTINCT statement and see the result.

## SELECT DISTINCT Examples

```sql
SELECT DISTINCT first_name
FROM patients;
```

The following SQL statement lists the number of different (distinct) first_name:

```sql
SELECT COUNT(DISTINCT first_name) FROM patients;
```

[← README.md](../README.md)