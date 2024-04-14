# SQL LOWER() Function

The LOWER() function returns the string in lowercase. Example: 'ExAmple' -> 'example'

Note: Depending on the language, LOWER may go by another name such as LCASE.

## Syntax

`LOWER(string)`

## Parameter Values

| Parameter | Description                     |
| --------- | ------------------------------- |
| string    | Required. The string to convert |

## LOWER() Example

The following SQL statement shows the first name of the patients in lowercase:

```sql
SELECT first_name, LOWER(first_name) AS lowercase_name
FROM patients;
```