# Get value from another table by custom function
## Create the Function
Here’s a simple function that counts the number of albums from a given artist:
``` SQL
CREATE FUNCTION [dbo].[ufn_AlbumCount] (@ArtistId int)  
RETURNS smallint
AS  
BEGIN  
    DECLARE @AlbumCount int;
    SELECT @AlbumCount = COUNT(AlbumId)
    FROM Albums
    WHERE ArtistId = @ArtistId; 
    RETURN @AlbumCount;
END;
GO
```
## Create the Computed Column
Now that I’ve created the function, I can add a computed column that references it.
``` SQL
ALTER TABLE Artists
ADD AlbumCount AS dbo.ufn_AlbumCount(ArtistId);
```
