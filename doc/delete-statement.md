# SQL DELETE Statement

[← README.md](../README.md)

The DELETE statement is used to delete existing records in a table.

## DELETE Syntax

`DELETE FROM tablename WHERE condition;`

Note: Be sure to specify the where clause. Failing to include the where clause will result in all of the rows to be deleted.

## SQL DELETE Example

The following SQL statement deletes all patients named "Paul" from the "patients" table:

```sql
DELETE FROM patients
WHERE first_name = 'Paul';
​
-- There are no longer any patients named 'Paul' in the database
SELECT * 
FROM patients 
WHERE first_name = 'Paul'
```

[← README.md](../README.md)