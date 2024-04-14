# SQL IN Operator

The IN operator allows you to specify multiple values in a WHERE clause.

The IN operator is a shorthand for multiple OR conditions.

## IN Syntax

```sql
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...);

-- or:
SELECT column_name(s)
FROM table_name
WHERE column_name IN (SELECT STATEMENT);
```

## IN Operator Examples

The following SQL statement selects all patients that are located in "SK", "AB" or "MB":

```sql
SELECT * FROM patients
WHERE province_id IN ('SK', 'AB', 'MB');
```

The following SQL statement selects all patients that are NOT located in "SK", "AB" or "MB":

```sql
SELECT * FROM patients
WHERE province_id NOT IN ('SK', 'AB', 'MB');
```

The following SQL statement selects all patients that have the same first_name as a doctor.

```sql
SELECT * FROM patients 
WHERE first_name IN (SELECT first_name FROM doctors)
-- Try running just the sub query to see the list
```