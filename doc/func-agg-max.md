# SQL MAX() Function

The MAX() function returns the largest value of the selected column.

## MAX() Syntax

```sql
SELECT MAX(column_name)
FROM table_name
WHERE condition;
```

## MAX() Example

The following SQL statement finds the highest patient's weight:

```sql
SELECT MAX(weight) FROM patients;
```