# Transactions
Pattern:
``` SQL
BEGIN TRANSACTION;
	actions...;
SAVE TRANSACTION PointName;
	actions...;
ROLLBACK TRANSACTION PointName;
COMMIT
```