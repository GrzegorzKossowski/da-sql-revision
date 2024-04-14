# SQL BETWEEN Operator

[← README.md](../README.md)

The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates.

The BETWEEN operator is inclusive: begin and end values are included.

```sql
SELECT column_name(s) FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```

The following SQL statement selects all patients with a weight between 100 and 120:

```sql
SELECT * FROM patients
WHERE weight BETWEEN 100 AND 120;
```

## NOT BETWEEN Example

To display the products outside the range of the previous example, use NOT BETWEEN:

```sql
SELECT * FROM patients
WHERE weight NOT BETWEEN 100 AND 120;
```

## BETWEEN with IN Example

The following SQL statement selects all patients with a weight between 100 and 120. In addition; do not show patients located in 'ON', 'SK', or 'AB':

```sql
SELECT * FROM patients
WHERE weight BETWEEN 100 AND 120
AND province_id NOT IN ('ON', 'SK', 'AB');
```

## Between with text

Text is compared based on the ASCII value of the text. For example, 'c'(99) is between 'a'(97) and 'e'(101) but 'C'(67) is not between 'a'(97) and 'e'(101).

The following SQL statement selects all patients with their first_name between 'Alex' and 'Ben'

```sql
SELECT * FROM patients
WHERE first_name BETWEEN 'Alex' AND 'Ben'
```

[← README.md](../README.md)