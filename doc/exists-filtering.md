# SQL EXISTS Operator

[← README.md](../README.md)

The EXISTS operator is used to test for the existence of any record in a subquery.

The EXISTS operator returns TRUE if the subquery returns one or more records.

Note: SQL statements that use the EXISTS condition are very inefficient since the sub-query is rerun for EVERY row in the outer query's table. There are more efficient ways to write most queries, that do not use the EXISTS condition.

## EXISTS Syntax

```sql
SELECT column_name(s)
  FROM table_name
  WHERE EXISTS
  (SELECT column_name FROM table_name WHERE condition);
```

## SQL EXISTS Examples

The following SQL statement returns all patients which was diagnosed with pregnancy.

```sql
SELECT * FROM patients 
  WHERE EXISTS (SELECT diagnosis FROM admissions 
      WHERE patients.patient_id = admissions.patient_id 
      AND diagnosis = 'Pregnancy')
```

The above SQL statement can be written more efficently:

```sql
SELECT * FROM patients 
  JOIN admissions ON patients.patient_id = admissions.patient_id
  WHERE diagnosis = 'Pregnancy'
```

[← README.md](../README.md)