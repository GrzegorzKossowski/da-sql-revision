# SQL ORDER BY Keyword

The ORDER BY keyword is used to sort the result-set in ascending or descending order.

The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword.

## ORDER BY Syntax

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

ORDER BY Example The following SQL statement selects all patients from the "Patients" table, sorted by the "first_name" column:

```sql
SELECT * FROM patients
ORDER BY first_name;
```

## ORDER BY DESC Example

The following SQL statement selects all patients from the "patients" table, sorted DESCENDING by the "first_name" column:

```sql
SELECT * FROM patients
ORDER BY first_name DESC;
```

## ORDER BY Several Columns 

The following SQL statement selects all patients from the "patients" table, sorted by the "first_name" and the "last_name" column. This means that it orders by first_name, but if some rows have the same first_name, it orders them by last_name:

```sql
SELECT * FROM patients
ORDER BY first_name, last_name;
```

The following SQL statement selects all patients from the "patients" table, sorted ascending by the "first_name" and descending by the "last_name" column:

```sql
SELECT * FROM patients
ORDER BY first_name ASC, last_name DESC;
```