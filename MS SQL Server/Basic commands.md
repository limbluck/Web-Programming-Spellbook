# Basic MS SQL Server query commands
## CREATE DATABASE
Creates a new database
Following line is enough
``` SQL
CREATE DATABASE DBName;
```
## CREATE TABLE
Creates a new table
Follow the pattern:
``` SQL
CREATE TABLE TableName (  
    Id int,  
    Column1 DATATYPE,  
    Column2 DATATYPE,  
    Column3 DATATYPE 
);
```
For more info about data types and keys and etc. see [[MS SQL Server/Data types|Data types]]
## INSERT INTO
Inserts new data into a database
Follow the pattern:
``` SQL
INSERT INTO TableName
(Column1Name, Column2Name, Column3Name, etc.)  
VALUES
(value1, value2, value3, etc.);
```
Empty insert:
``` SQL
INSERT INTO TableName DEFAULT VALUES;
```
## SELECT
Extracts data from a database
Follow the pattern:
``` SQL
SELECT
conditions
FROM
dbo.TableName;
```
For conditions see [[MS SQL Server/Filtering|Filtering]]
## UPDATE
Updates data in a database
Follow the pattern:
``` SQL
UPDATE TableName
SET
	Column1Name = value1,
	Column2Name = value2,
	etc.  
WHERE
	conditions;
```
For conditions see [[MS SQL Server/Filtering|Filtering]]
## DELETE
Deletes data from a database
Follow the pattern:
``` SQL
DELETE FROM TableName WHERE
	condition;
```
For conditions see [[MS SQL Server/Filtering|Filtering]]
## DROP
Deletes a table
Following line is enough:
``` SQL
For tables:
	DROP TABLE TableName;
For columns:
	ALTER TABLE TableName
		DROP COLUMN ColumnName;
For constraints:
	ALTER TABLE TableName
		DROP CONSTRAINT ConstraintName;
For indexes:
	ALTER TABLE TableName
		DROP INDEX IndexName;
```
## ALTER TABLE
Modifies a table
Follow the pattern: 
``` SQL
ALTER TABLE TableName  
	other commands
```
## ADD
Add a column in an existing table
Follow the pattern:
``` SQL
ALTER TABLE TableName
	ADD ColumnName DataType;
```
[[MS SQL Server/Constraints|To add constraints follow me]]
## CREATE INDEX
Creates an index (search key)
Follow the pattern: 
``` SQL
CREATE UNIQUE INDEX IndexName  
ON TableName (Column1, Column2, etc.);
```