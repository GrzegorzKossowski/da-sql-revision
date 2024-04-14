# SQL GROUP BY Statement

[← README.md](../README.md)

The GROUP BY statement groups rows that have the same values into summary rows, like "find the number of patients in each province".

The GROUP BY statement is often used with aggregate functions (`COUNT()`, `MAX()`, `MIN()`, `SUM()`, `AVG()`) to group the result-set by one or more columns.

## GROUP BY Syntax

```sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
```

## SQL GROUP BY Examples

The following SQL statement lists the number of patients in each province:

```sql
SELECT COUNT(*), province_id
FROM patients
GROUP BY province_id;
```

The following SQL statement lists the number of patients in each country, sorted high to low:

```sql
SELECT COUNT(*), province_id
FROM patients
GROUP BY province_id
ORDER BY COUNT(*) DESC;
```

[← README.md](../README.md)