# SQL COUNT() Function

The COUNT() function returns the number of rows that matches a specified criterion.

COUNT() usually has * as it's parameter because the name of the column does not usually matter since they all have the same count.

## COUNT() Syntax

```
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
```

## COUNT() Example

The following SQL statement finds the number of patients that weight over 120Kg:

```sql
SELECT COUNT(*) FROM patients 
WHERE weight > 120;
```