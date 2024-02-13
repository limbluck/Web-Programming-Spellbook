# Enable FILESTREAM

1. On the **Start** menu, navigate to **All Programs > SQL Server > Configuration Tools**, and then select **SQL Server Configuration Manager**.
    
2. In the list of services, right-click **SQL Server Services**, and then select **Open**.
    
3. In the **SQL Server Configuration Manager** snap-in, locate the instance of SQL Server on which you want to enable FILESTREAM.
    
4. Right-click the instance, and then select **Properties**.
    
5. In the **SQL Server Properties** dialog box, select the **FILESTREAM** tab.
    
6. Select the **Enable FILESTREAM for Transact-SQL access** check box.
    
7. If you want to read and write FILESTREAM data from Windows, select **Enable FILESTREAM for file I/O streaming access**. Enter the name of the Windows share in the **Windows Share Name** box.
    
8. If remote clients must access the FILESTREAM data that is stored on this share, select **Allow remote clients to have streaming access to FILESTREAM data**.
    
9. Select **Apply**.
    
10. In SQL Server Management Studio, select **New Query** to display the Query Editor.
    
11. In Query Editor, enter the following Transact-SQL code:
    ``` SQL
    EXEC sp_configure filestream_access_level, 2;
    RECONFIGURE;
    ```
    
12. Select **Execute**.
    
13. Restart the SQL Server service.