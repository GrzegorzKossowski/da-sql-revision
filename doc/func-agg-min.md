# SQL Min() Function

The MIN() function returns the smallest value of the selected column.

## MIN() Syntax

```sql
SELECT MIN(column_name)
FROM table_name
WHERE condition;
```

## MIN() Example

The following SQL statement finds the lowest patient's weight:

```sql
SELECT MIN(weight) FROM patients;
```