# SQL RAND() Function

The RAND() function returns a random number between 0 and 1

Note: Depending on the language, RAND may go by another name such as RANDOM. Check with your language to verify.

## Syntax

`RAND(seed)`

## Parameter Values

| Parameter | Description                                                                                                                                        |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| seed      | Optional. If seed is specified, it returns a repeatable sequence of random numbers. If no seed is specified, it returns a completely random number |

## RAND() Example

The following SQL statement displays a random number between 0-1:

`SELECT RAND();`
