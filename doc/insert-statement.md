# SQL INSERT Statement

[← README.md](../README.md)

INSERT INTO statement is used to insert new records in a table.

## INSERT INTO Syntax

It is possible to write the INSERT INTO statement in two ways:

1. Specify both the column names and the values to be inserted:

    `INSERT INTO tablename (column1, column2, column3, ...)
    VALUES (value1, value2, value3, ...);`

2. If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the INSERT INTO syntax would be as follows:

    `INSERT INTO tablename
    VALUES (value1, value2, value3, ...);`

## INSERT INTO Example

The following SQL statement inserts a new record in the patients table:

```sql
-- Insert a record
INSERT INTO patients 
(first_name, last_name, gender, birth_date, city, province_id, allergies, weight, height)
VALUES
('John', 'Smith', 'M', '1994-02-21', 'Hamilton','ON', NULL, 132, 182);
 
-- Select the most recent record by id to display it.
SELECT * 
FROM patients
WHERE patient_id = (SELECT MAX(patient_id) FROM patients);
```

## Insert Data Only in Specified Columns
It is also possible to only insert data in specific columns.

If the table column allow for NULL values then you do not need to include the column in your insert statement.

The following SQL statement will insert a new record, but only insert data in the "first_name", "last_name", and "gender" columns (patient_id will be updated automatically):

```sql
-- Insert a record
INSERT INTO patients 
(first_name, last_name, gender)
VALUES ('Jane', 'Doe','F');
    
-- Select the most recent record by id to display it.
SELECT * FROM patients
WHERE patient_id = (SELECT MAX(patient_id) FROM patients);
```

[← README.md](../README.md)
