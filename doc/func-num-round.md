# SQL ROUND() Function

The ROUND() function returns the input decimal number rounded to the nearest defined decimal position.

# Syntax

`ROUND(number, deciamls)`

## Parameter Values

| Parameter | Description                                                                                                 |
| --------- | ----------------------------------------------------------------------------------------------------------- |
| number    | Required. A numeric value                                                                                   |
| number    | Optional. The number of decimal places to round number to. If omitted, it returns the integer (no decimals) |

## ROUND() Example

The following SQL statement rounds 135.375 to the nearest 2 decimal places.

`SELECT ROUND(135.375, 2);`
