# SQL Aliases

[← README.md](../README.md)

SQL aliases are used to give a table, or a column in a table, a temporary name.

Aliases are often used to make column names more readable.

An alias only exists for the duration of that query.

An alias is created with the AS keyword.

Depending on the language, the AS keyword is optional.

## Alias Column Syntax

```sql
SELECT column_name AS alias_name
FROM table_name;
```

## Alias Table Syntax

```sql
SELECT column_name(s)
FROM table_name AS alias_name;
```

## Alias for Columns Examples

The following SQL statement creates two aliases, one for the CustomerID column and one for the CustomerName column:

```sql
SELECT AVG(weight) AS average_weight, 
       AVG(height) AS average_height
FROM patients;
```

## Alias for Tables Example

The following SQL renames the admissions table as 'a' and the patients as 'p'

```sql
SELECT *
FROM patients AS p
JOIN admissions AS a ON a.patient_id = p.patient_id;
```

[← README.md](../README.md)