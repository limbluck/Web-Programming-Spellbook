# Controller
## What is it
**MVC controllers** are responsible for responding to requests made against an ASP.NET MVC website
Controllers should not contain any data logic, this is the job for [[dotNET/API Backend/Service|Services]]
A controller with data logic is a fat controller
## How to use it
Create new .cs file with a controller class with API request methods
Sample:
``` C#
using Microsoft.AspNetCore.Mvc;

[ApiController]
[Route("api/[controller]")]
public class NameController : ControllerBase
{
	[HttpMethod]
	[Route("{attribute}")]
	public async Task<ActionResult<ServiceResponce<Model>>> Method(int attribute)
	{
		// Some api logic
	    return Response(await Service.Method(attribute));
	}
}
```