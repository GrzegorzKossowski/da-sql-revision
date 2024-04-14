# SQL First_Value() Window Function

The FIRST_VALUE() function is a window function that returns the first value in an ordered partition of a result set.

## Syntax

```
FIRST_VALUE ( scalar_expression )
OVER (
    [PARTITION BY partition_expression, ... ]
    ORDER BY sort_expression [ASC | DESC], ...
)
```

## Parameter Values

| Parameter         | Description                                                                                                                                                                                                                                                      |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| scalar_expression | Required. scalar_expression is an expression evaluated against the value of the first row in an ordered partition of the result set. The scalar_expression can be a column, subquery, or expression evaluates to a single value. It cannot be a window function. |

## FIRST_VALUE() Example

The following SQL statement displays the oldest patient's birth_date for the province the patient is in.

```sql
SELECT
patient_id,
province_id,
FIRST_VALUE(birth_date)
OVER(PARTITION BY province_id -- group by province_id
ORDER BY birth_date -- order it by birth_date for the first_value
-- select all rows in the partiton
ROWS BETWEEN UNBOUNDED PRECEDING AND UNBOUNDED FOLLOWING
) AS oldest_birth_date
FROM patients
ORDER BY patient_id;
```
