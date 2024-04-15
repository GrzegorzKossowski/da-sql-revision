# SQL DEFAULT Constraint

[← README.md](../README.md)

The DEFAULT constraint is used to set a default value for a column.

The default value will be added to all new records, if no other value is specified.

## SQL DEFAULT on CREATE TABLE

The following SQL sets a DEFAULT value for the "City" column when the "Persons" table is created:

### My SQL / SQL Server / Oracle / MS Access:

```sql
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255) DEFAULT 'Sandnes'
);
```

The DEFAULT constraint can also be used to insert system values, by using functions like current_timestamp:

### MySQL / SQL Server / Oracle / MS Access:

```sql
CREATE TABLE Orders (
    ID int NOT NULL,
    OrderNumber int NOT NULL,
    OrderDate date DEFAULT current_timestamp
);
INSERT INTO Orders (ID,OrderNumber) VALUES (1,1);
SELECT * FROM Orders;
```

## SQL DEFAULT on ALTER TABLE

To create a DEFAULT constraint on the "City" column when the table is already created, use the following SQL:

### MySQL:

```sql
ALTER TABLE Persons
ALTER City SET DEFAULT 'Sandnes';
```

To allow naming of a CHECK constraint, and for defining a CHECK constraint on multiple columns, use the following SQL syntax:

### SQL Server:

```sql
ALTER TABLE Persons
ADD CONSTRAINT df_City
DEFAULT 'Sandnes' FOR City;
```

### MS Access:

```sql
ALTER TABLE Persons
ALTER COLUMN City SET DEFAULT 'Sandnes';
```

### Oracle:

```sql
ALTER TABLE Persons
MODIFY City DEFAULT 'Sandnes';
```

## DROP a DEFAULT Constraint

To drop a DEFAULT constraint, use the following SQL:

### MySQL:

```sql
ALTER TABLE Persons
ALTER City DROP DEFAULT;
```

### SQL Server / Oracle / MS Access:

```sql
ALTER TABLE Persons
ALTER COLUMN City DROP DEFAULT;
```

[← README.md](../README.md)