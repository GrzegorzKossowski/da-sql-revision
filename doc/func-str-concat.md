# SQL CONCAT() Function

The CONCAT() function adds two or more expressions together.

Note: Depending on the language there may be a built in syntax support for concat. Eg, + or ||

## Syntax

`CONCAT(expression1, expression2, expression3,...)`

## Parameter Values

| Parameter                                   | Description                                                                                                 |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| expression1, expression2, expression3, etc. | Required. The expressions to add together. Note: If any of the expressions is a NULL value, it returns NULL |

## CONCAT() Example

The following SQL statement concats the first_name and last_name of each patient together:

```sql
SELECT CONCAT(first_name,' ', last_name) AS full_name
FROM patients;
```