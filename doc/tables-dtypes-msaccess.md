# MS Access Data Types

[← README.md](../README.md)

-   [mysql](tables-dtypes-mysql.md)
-   [SQL Server](tables-dtypes-sqlserver.md)
-   [MS Access](tables-dtypes-msaccess.md)

| Data type                                                                                    | Description                                                                                                                                                                               | Storage |
| -------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| Text                                                                                         | Use for text or combinations of text and numbers. 255 characters maximum                                                                                                                  |         |
| Memo                                                                                         | Memo is used for larger amounts of text. Stores up to 65,536 characters. Note: You cannot sort a memo field. However, they are searchable                                                 |         |
| Byte                                                                                         | Allows whole numbers from 0 to 255                                                                                                                                                        | 1 byte  |
| Integer                                                                                      | Allows whole numbers between -32,768 and 32,767                                                                                                                                           | 2 bytes |
| Long                                                                                         | Allows whole numbers between -2,147,483,648 and 2,147,483,647                                                                                                                             | 4 bytes |
| Single                                                                                       | Single precision floating-point. Will handle most decimals                                                                                                                                | 4 bytes |
| Double                                                                                       | Double precision floating-point. Will handle most decimals                                                                                                                                | 8 bytes |
| Currency                                                                                     | Use for currency. Holds up to 15 digits of whole dollars, plus 4 decimal places. Tip: You can choose which country's currency to use                                                      | 8 bytes |
| AutoNumber                                                                                   | AutoNumber fields automatically give each record its own number, usually starting at 1                                                                                                    | 4 bytes |
| Date/Time                                                                                    | Use for dates and times                                                                                                                                                                   | 8 bytes |
| Yes/No                                                                                       | A logical field can be displayed as Yes/No, True/False, or On/Off. In code, use the constants True and False (equivalent to -1 and 0). Note: Null values are not allowed in Yes/No fields | 1 bit   |
| Ole                                                                                          | Object Can store pictures, audio, video, or other BLOBs (Binary Large OBjects) up to                                                                                                      | 1GB     |
| Hyperlink                                                                                    | Contain links to other files, including web pages                                                                                                                                         |
| Lookup Wizard| Let you type a list of options, which can then be chosen from a drop-down list | 4 bytes                                                                                                                                                                                   |


[← README.md](../README.md)