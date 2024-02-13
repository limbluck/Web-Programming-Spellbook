# Constraints
## Constraint
SQL constraints are used to specify rules for data in a table.
To view constraints:
``` SQL
sp_help TableName;
sp_helpconstraint TableName;
```
## Primary key
A combination of a `NOT NULL` and `UNIQUE`. Uniquely identifies each row in a table
Default syntax is: PK_TableName_16SymbolsKey
Create in an existing table:
``` SQL
ALTER TABLE TableName
	ADD CONSTRAINT PK_ConstraintName PRIMARY KEY (ColumnName)
;
```
Create in a new table:
``` SQL
CREATE TABLE TableName(
	ColumnName DataType,
		CONSTRAINT PK_ConstraintName PRIMARY KEY (ColumnName)
);
```
## Auto increment
To create an auto-counter on a field use `IDENTITY (seed, increment)`
``` SQL
CREATE TABLE TableName(
ID INT IDENTITY(1, 1),
...
);
```
## Foreign key
Prevents actions that would destroy links between tables
Default syntax is: FK_TableName_16SymbolsKey
Create in an existing table:
``` SQL
ALTER TABLE TableName
	ADD
		ColumnName INT,
			CONSTRAINT FK_ConstraintName FOREIGN KEY (ColumnName)
			REFERENCES AnotherTableName(AnotherTableColumnName)
;
```
Create in a new table:
``` SQL
CREATE TABLE TableName(
	..
	ColumnName DataType,
		CONSTRAINT FK_ConstraintName FOREIGN KEY (ColumnName)
		REFERENCES AnotherTableName(AnotherTableColumnName),
	..
);
```
## Not null
Ensures that a column cannot have a NULL value
Alter in an existing table:
``` SQL
ALTER TABLE TableName
	ALTER COLUMN ColumnName DataType NOT NULL DEFAULT DefaultValue
;
```
Create in a new table:
``` SQL
CREATE TABLE TableName(
	..
	ColumnName DataType NOT NULL,
	..
);
```
## Unique
Ensures that all values in a column are different
Default syntax is: UQ_TableName_16SymbolsKey
Alter in an existing table:
``` SQL
ALTER TABLE TableName
	ADD CONSTRAINT UQ_ConstraintName UNIQUE (ColumnName1, ColumnName2, etc...);

```
Create in a new table:
``` SQL
CREATE TABLE TableName(
	..
	ADD CONSTRAINT UQ_ConstraintName UNIQUE (ColumnName1, ColumnName2, etc...),
	..
);
```
## Check
Ensures that the values in a column satisfies a specific condition
Default syntax is: FK_TableName_KeyName_16SymbolsKey
Alter in an existing table:
``` SQL
ALTER TABLE TableName
	ADD CONSTRAINT CK_ConstraintName CHECK (condition);

```
Create in a new table:
``` SQL
CREATE TABLE TableName (  
    ... 
    CONSTRAINT CK_ConstraintName CHECK (condition);
    ...  
);
```
## Default
Sets a default value for a column if no value is specified
Default syntax is: DF_TableName_KeyName_16SymbolsKey
Alter in an existing table:
``` SQL
ALTER TABLE TableName
	ADD CONSTRAINT DF_ConstraintName DEFAULT value FOR ColumnName;
```
Create in a new table:
``` SQL
CREATE TABLE TableName (  
    ... 
    ColumnName DataType DEFAULT value,
    ...  
);
```