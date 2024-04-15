# SQL DROP TABLE Statement

[← README.md](../README.md)

The DROP TABLE statement is used to drop an existing table in a database.

## Syntax

`DROP TABLE table_name;`

Note: Be careful before dropping a table. Deleting a table will result in loss of complete information stored in the table!

## SQL DROP TABLE Example

The following SQL statement drops the existing table "patients":

```sql
DROP TABLE patients;
​
-- try to query the table.
SELECT * FROM patients
```

[← README.md](../README.md)