# To create a table to store FILESTREAM data

1. In SQL Server Management Studio, click **New Query** to display the Query Editor.
    
2. Copy the Transact-SQL code from the following example into the Query Editor. This Transact-SQL code creates a FILESTREAM-enabled table called Records.
    
3. To create the table, click **Execute**.
# Example
``` SQL
CREATE TABLE Archive.dbo.Records(
	[Id] [uniqueidentifier] ROWGUIDCOL NOT NULL UNIQUE, 
	[SerialNumber] INTEGER UNIQUE, 
	[Chart] VARBINARY(MAX) FILESTREAM NULL 
); GO
```