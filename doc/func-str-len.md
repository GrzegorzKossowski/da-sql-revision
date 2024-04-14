# SQL LEN() Function

The LEN() function returns the length of the string in bytes.

Note: Depending on the language, LEN may go by another name such as LENGTH.

## Syntax

`LEN(string)`

## Parameter Values

| Parameter | Description                                  |
| --------- | -------------------------------------------- |
| string    | Required. The string to count the length for |

## LEN() Example

The following SQL statement shows the first name of the patients and the length of their name:

```sql
SELECT first_name, LEN(first_name) AS length_of_name
FROM patients;
```