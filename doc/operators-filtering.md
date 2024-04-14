# SQL AND, OR and NOT Operators

The WHERE clause can be combined with AND, OR, and NOT operators.

The AND and OR operators are used to filter records based on more than one condition:

- The AND operator displays a record if all the conditions separated by AND are TRUE.

- The OR operator displays a record if any of the conditions separated by OR is TRUE.

- The NOT operator displays a record if the condition(s) is NOT TRUE.

## AND Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
```

## OR Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
```

## NOT Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```

## AND Example

The following SQL statement selects all fields from "patients" where first_name is "John" AND city is "Toronto":

```sql
SELECT * FROM patients
WHERE first_name='John' AND city='Toronto';
```

## OR Example

The following SQL statement selects all fields from "patients" where city is "Hamilton" OR "Toronto":

```sql
SELECT * FROM patients
WHERE city='Hamilton' OR city='Toronto';
```

## NOT Example

The following SQL statement selects all fields from "patients" where province_id is NOT "ON" (Ontario):

```sql
SELECT * FROM patients
WHERE NOT province_id = 'ON';
```