# Service
## What is it
Services are responsible for the data related logic
## How to use it
Create new .cs file with a class and an interface for it, for example:
### Interface:
``` C#
public interface IService
{
    Task<ServiceResponce<Data>> Method1();
    Task<ServiceResponce<Data>> Method2();
}
```
### Class:
``` C#
public class Service : IService
{
	Task<ServiceResponce<Data>> Method1()
	{
		// Some logic
		return responce
	}
    Task<ServiceResponce<Data>> Method2()
    {
	    // Some logic
		return responce
    }
}
```
### Scope them in Program.cs
``` C#
builder.Services.AddScoped<IService, Service>();
```