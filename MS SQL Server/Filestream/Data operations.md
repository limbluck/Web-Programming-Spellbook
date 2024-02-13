# Data operations
## Insert NULL

The following example shows how to insert `NULL`. When the FILESTREAM value is `NULL`, the Database Engine doesn't create a file in the file system.

``` SQL
INSERT INTO Archive.dbo.Records
    VALUES (NEWID(), 1, NULL);
GO
```
## Insert a zero-length record

The following example shows how to use `INSERT` to create a zero-length record. This is useful for when you want to obtain a file handle, but will be manipulating the file by using Win32 APIs.

``` SQL
INSERT INTO Archive.dbo.Records
    VALUES (NEWID(), 2, 
      CAST ('' AS VARBINARY(MAX)));
GO
```
## Insert existing data

In this example, we will insert a picture which is located at the `C:\\sqlshack` folder.

``` SQL
DECLARE @File varbinary(MAX);

SELECT  @File = CAST(bulkcolumn as varbinary(max))
	FROM OPENROWSET(BULK 'C:\sqlshack\akshita.png', SINGLE_BLOB) as MyData; 
 
INSERT INTO Archive.dbo.Records VALUES  
(NEWID(), 4, @File)
```

## Create a data file

The following example shows how to use `INSERT` to create a file that contains data. The Database Engine converts the string `Seismic Data` to a `varbinary(max)` value. FILESTREAM creates the Windows file if it doesn't already exist. The data is then added to the data file.

``` SQL
INSERT INTO Archive.dbo.Records
    VALUES (NEWID(), 3, 
      CAST ('Seismic Data' AS VARBINARY(MAX)));
GO
```
## Update  data

You can use Transact-SQL to update the data in the file system file, but you might not want to when streaming large amounts of data to a file.

The following example replaces any text in the file record with the text `Xray 1`.

``` SQL
UPDATE Archive.dbo.Records
SET [Chart] = CAST('Xray 1' AS VARBINARY(MAX))
WHERE [SerialNumber] = 2;
```
## Delete data

When you delete a row that contains a FILESTREAM field, you also delete its underlying file system files. The only way to delete a row, and therefore the file, is to use the Transact-SQL DELETE statement.

The following example shows how to delete a row and its associated file system files.

``` SQL
DELETE Archive.dbo.Records
WHERE SerialNumber = 1;
GO
```
