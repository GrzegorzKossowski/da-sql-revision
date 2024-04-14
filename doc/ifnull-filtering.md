# SQL IFNULL(), ISNULL(), COALESCE(), and NVL() Functions

[← README.md](../README.md)

The `IFNULL` function goes by many names depending on what language you are using. We use `IFNULL` but your specific language may use, `ISNULL`, `COALESCE`, or `NVL` but most function the same.

Look at the following `SELECT` statement:

```sql
​SELECT first_name, allergies
FROM patients
```

The allergie column displays null for our output in some cases. We want it to display a default value in that case

## Solutions

### MySQL

The MySQL `IFNULL()` function lets you return an alternative value if an expression is NULL:

```sql
SELECT first_name, IFNULL(allergies,'none') AS allergies 
FROM patients

-- or we can use the COALESCE() function, like this:

SELECT first_name, COALESCE(allergies,'none') AS allergies 
FROM patients
```

### SQL Server

The SQL Server `ISNULL()` function lets you return an alternative value when an expression is NULL:

```sql
SELECT first_name, IFNULL(allergies,'none') AS allergies 
FROM patients
```

### MS Access

The MS Access `IsNull()` function returns TRUE (1) if the expression is a null value, otherwise FALSE (0):

```sql
SELECT first_name, IIF(ISNULL(allergies,0),allergies) AS allergies 
FROM patients
```

### Oracle

The Oracle `NVL()` function achieves the same result:

```sql
SELECT first_name, NVL(allergies,'none') AS allergies 
FROM patients
```

[← README.md](../README.md)