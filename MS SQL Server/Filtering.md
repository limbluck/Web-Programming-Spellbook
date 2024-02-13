# Filtering
## Main filters
Sample filter:
``` SQL
SELECT Columns FROM TableWHERE
	conditions;
	GROUP BY Column  HAVING
		conditions
		ORDER BY Column
;
```
## Select top
Select top records
``` SQL
SELECT TOP 3 * FROM TableName;
```
## Limit
Limit 3 records
``` SQL
SELECT * FROM TableName  
	LIMIT 3;
```
## Order by
Set order in descending or ascending
``` SQL
SELECT 3 * FROM TableName  
	ORDER BY ColumnName DESC/ASC;
```
## DISTINCT
Get only unique values
``` SQL
SELECT DISTINCT ColumnName1, ColumnName2, etc. FROM TableName;
```
## AS
Set alias
``` SQL
SELECT TN1.ColumnName1, TN1.ColumnName2, TN2.ColumnName1, etc.
FROM TableName1 AS TN1, TableName2 AS TN2  
WHERE TN1.ColumnName1 = condition etc.
;
```