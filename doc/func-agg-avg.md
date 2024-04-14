# SQL AVG() Function

The AVG() function returns the average value of a numeric column.

## AVG() Syntax

```sql
SELECT AVG(column_name)
FROM table_name
WHERE condition;
```

## AVG() Example

The following SQL statement finds the average weight of patients:

```sql
SELECT AVG(weight) FROM patients;
```