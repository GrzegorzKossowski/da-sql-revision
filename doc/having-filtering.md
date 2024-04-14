# SQL HAVING Clause

[← README.md](../README.md)

The HAVING clause was added to SQL because the WHERE keyword cannot be used with aggregate functions.

## HAVING Syntax

```sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```

## SQL HAVING Examples

The following SQL statement lists the names of patients with a common first_name (> 30 occurances).

```sql
SELECT COUNT(*), first_name
FROM patients
GROUP BY first_name
HAVING COUNT(*) > 30;
```

The following SQL statement lists the names of patients with a common first_name (> 30 occurances). Sorted high to low:

```sql
SELECT COUNT(*), first_name
FROM patients
GROUP BY first_name
HAVING COUNT(*) > 30
ORDER BY COUNT(*) DESC;
```

[← README.md](../README.md)