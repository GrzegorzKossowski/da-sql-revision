# SQL UPDATE Statement

[← README.md](../README.md)

The UPDATE statement is used to modify the existing records in a table.

## UPDATE Syntax

```sql
UPDATE tablename
SET column1 = value1, column2 = value2, ...
WHERE condition;
```
Note: Be sure to specify the where clause. Failing to include the where clause will result in all of the rows to be updated.

The following SQL statement updates the first patient (patient_id = 1) with a new first_name and a new weight.


```sql
UPDATE patients
SET first_name = 'John', weight = 120
WHERE patient_id = 1;
​
-- display the patient we just updated
SELECT * FROM patients WHERE patient_id = 1;
```


## UPDATE Multiple Records

It is the WHERE clause that determines how many records will be updated.

The following SQL statement will update the allergies to 'NKA' (no known allergies) for all records where allergies is NULL

```sql
UPDATE patients
SET allergies = 'NKA'
WHERE allergies IS NULL;
​
-- display the patients table
SELECT * FROM patients;
```

[← README.md](../README.md)