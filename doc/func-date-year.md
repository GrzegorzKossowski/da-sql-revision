# SQL Year() Function

The YEAR() function returns the year part for a given date (a number from 1000 to 9999).

## Syntax

`YEAR(date)`

##Parameter Values

| Parameter | Description                                 |
| --------- | ------------------------------------------- |
| date      | Required. The date to extract the year from |

## YEAR() Example

The following SQL statement shows the current year we're in:

`SELECT YEAR(current_timestamp)`