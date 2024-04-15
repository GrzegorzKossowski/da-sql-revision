# SQL ALTER TABLE Statement

[← README.md](../README.md)

The ALTER TABLE statement is used to add, delete, or modify columns in an existing table.

The ALTER TABLE statement is also used to add and drop various constraints on an existing table.

## ALTER TABLE - ADD Column Syntax

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

The following SQL adds an "Email" column to the "patients" table:

```sql
ALTER TABLE patients
ADD email varchar(255);
​
SELECT patient_id, email FROM patients;
```

## ALTER TABLE - DROP COLUMN Syntax

To delete a column in a table, use the following syntax (Note: Some database systems don't allow deleting a column):

```sql
ALTER TABLE table_name
DROP COLUMN column_name;
```

The following SQL deletes the "last_name" column from the "patients" table:

```sql
ALTER TABLE patients
DROP COLUMN last_name;
​
SELECT * FROM patients
```

## ALTER TABLE - ALTER/MODIFY COLUMN Syntax

To change the data type of a column in a table, use the following syntax:

### SQL Server / MS Access:

```sql
ALTER TABLE table_name
ALTER COLUMN column_name datatype;
```

### My SQL / Oracle (prior version 10G):

```sql
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;
```

### Oracle 10G and later:

```sql
ALTER TABLE table_name
MODIFY column_name datatype;
```

[← README.md](../README.md)