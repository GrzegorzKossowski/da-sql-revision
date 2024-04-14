# SQL UPPER() Function

The UPPER() function returns the string in uppercase. Example: 'ExAmple' -> 'EXAMPLE'

Note: Depending on the language, UPPER may go by another name such as UCASE.

## Syntax

`UPPER(string)`

## Parameter Values

| Parameter | Description                     |
| --------- | ------------------------------- |
| string    | Required. The string to convert |

## UPPER() Example

The following SQL statement shows the first name of the patients in uppercase:

```sql
SELECT first_name, UPPER(first_name) AS uppercase_name
FROM patients;
```