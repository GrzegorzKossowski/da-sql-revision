# SQL LIKE Operator

The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.

There are two wildcards often used in conjunction with the LIKE operator:

- The percent sign `%` represents zero, one, or multiple characters

- The underscore sign `_` represents one, single character

The percent sign and the underscore can also be used in combinations

## LIKE Syntax

```sql
SELECT column1, column2, ...
FROM table_name
WHERE COLUMN LIKE pattern;
```

Here are some examples showing different LIKE operators with '%' and '_' wildcards:

|LIKE Operator|	Description|
|-|-|
|WHERE first_name LIKE 'a%'	|Finds any values that start with "a"|
|WHERE first_name LIKE '%a'	|Finds any values that end with "a"|
|WHERE first_name LIKE '%or%'	|Finds any values that have "or" in any position|
|WHERE first_name LIKE '_r%'	|Finds any values that have "r" in the second position|
|WHERE first_name LIKE 'a_%'	|Finds any values that start with "a" and are at least 2 characters in length|
|WHERE first_name LIKE 'a__%'	|Finds any values that start with "a" and are at least 3 characters in length|
|WHERE first_name LIKE 'a%o'	|Finds any values that start with "a" and ends with "o"|

## SQL LIKE Examples

The following SQL statement selects all patients with a first_name starting with "a":

```sql
SELECT * FROM patients
WHERE first_name LIKE 'a%';
```

The following SQL statement selects all patients with a first_name ending with "a":

```sql
SELECT * FROM patients
WHERE first_name LIKE '%a';
```

The following SQL statement selects all patients with a first_name that have "or" in any position:

```sql
SELECT * FROM patients
WHERE first_name LIKE '%or%';
```

The following SQL statement selects all patients with a first_name that have "r" in the second position:

```sql
SELECT * FROM patients
WHERE first_name LIKE '_r%';
```

The following SQL statement selects all patients with a first_name that starts with "a" and are at least 3 characters in length:

```sql
SELECT * FROM patients
WHERE first_name LIKE 'a__%';
```

The following SQL statement selects all patients with a first_name that starts with "a" and ends with "o":

```sql
SELECT * FROM patients
WHERE first_name LIKE 'a%o';
```

The following SQL statement selects all patients with a first_name that does NOT start with "a":

```sql
SELECT * FROM patients
WHERE first_name NOT LIKE 'a%';
```