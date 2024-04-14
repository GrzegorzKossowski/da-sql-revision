# SQL Lead() Window Function

The Lead() function returns the record offsetted by the specified amount.

## Syntax

`LEAD(expression [, OFFSET])`

## Parameter Values

| Parameter  | Description                                                                                                                                                                                                                                                                         |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| expression | Required. The value to be returned based on the specified offset. It is an expression of any type that returns a single (scalar) value. expression cannot be an analytic function.                                                                                                  |
| offset     | Optional. The number of rows forwards from the current row from which to obtain a value. If not specified, the default is 1. offset can be a column, subquery, or other expression that evaluates to a positive integer. offset cannot be a negative value or an analytic function. |

## Lead() Example

The following SQL statement displays every patients first_name and the patient's first_name after them.

```sql
SELECT
patient_id,
first_name,
LEAD(first_name, 1) OVER() AS next_name
FROM patients;
```