# SQL SUM() Function

The SUM() function returns the total sum of a numeric column.

## SUM() Syntax

```sql
SELECT SUM(column_name)
FROM table_name
WHERE condition;
```

## SUM() Example

The following SQL statement finds the sum of patients weight:

```sql
SELECT SUM(weight) FROM patients;
```