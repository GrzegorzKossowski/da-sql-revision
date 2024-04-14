# SQL UNION Operator

The UNION operator is used to combine the result-set of two or more SELECT statements.

- Every SELECT statement within UNION must have the same number of columns

- The columns must also have similar data types

- The columns in every SELECT statement must also be in the same order

## UNION Syntax

```sql
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```

## UNION ALL Syntax

The UNION operator selects only distinct values by default. To allow duplicate values, use UNION ALL:

```sql
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;
```

Note: The column names in the result-set are usually equal to the column names in the first SELECT statement.

## SQL UNION Example

The following SQL statement returns the first_names (only distinct values) from both the "patients" and the "doctors" table:

```sql
SELECT first_name FROM patients
UNION 
SELECT first_name FROM doctors
ORDER BY first_name;
```

## SQL UNION ALL Example

The following SQL statement returns the first_names (duplicate values also) from both the "patients" and the "doctors" table:

```sql
SELECT first_name FROM patients
UNION ALL
SELECT first_name FROM doctors
ORDER BY first_name;
```