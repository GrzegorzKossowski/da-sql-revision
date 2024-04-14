# SQL NULL Values

[← README.md](../README.md)

**What is a NULL Value?**

A field with a NULL value is a field with no value.

If a field in a table is optional, it is possible to insert a new record or update a record without adding a value to this field. Then, the field will be saved with a NULL value.

**How to Test for NULL Values?**

It is not possible to test for NULL values with comparison operators, such as =, <, or <>.

We will have to use the IS NULL and IS NOT NULL operators instead.

## IS NULL Syntax

```sql
SELECT column_names
FROM table_name
WHERE column_name IS NULL;
```

## IS NOT NULL Syntax

```sql
SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;
```

## The IS NULL Operator

The IS NULL operator is used to test for empty values (NULL values).

The following SQL lists all patients with a NULL value in the "allergies" field:

```sql
SELECT *
FROM patients
WHERE allergies IS NULL;
```

[← README.md](../README.md)