For better error handling with [[dotNET/API Backend/Service responce|Service responce]] use try/catch:
``` C#
method Method()
{
	// Some unbreakable code
	try
	{
	    // Some code
	    if (error)
	    {
	        throw new Exception("Error message");
	    }
	    // Some code
	}
	catch (Exception ex)
	{
	    serviceResponce.Success = false;
	    serviceResponce.Message = ex.Message;
	}
	return serviceResponce;
}
```