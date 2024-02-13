# To create a FILESTREAM-enabled database

1. In SQL Server Management Studio, click **New Query** to display the Query Editor.
    
2. Copy the Transact-SQL code from the following example into the Query Editor. This Transact-SQL code creates a FILESTREAM-enabled database called Archive.
    
    For this script, the directory C:\Data must exist.
    
3. To build the database, click **Execute**.

## Example 
``` SQL
CREATE DATABASE Archive 
ON
PRIMARY ( NAME = Arch1,
    FILENAME = 'C:\data\archdat1.mdf'),
FILEGROUP FileStreamGroup1 CONTAINS FILESTREAM ( NAME = Arch3,
    FILENAME = 'C:\data\filestream1')
LOG ON  ( NAME = Archlog1,
    FILENAME = 'C:\data\archlog1.ldf')
GO
```