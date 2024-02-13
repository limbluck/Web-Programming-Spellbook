# Service responce
## What is it
Data type for better frontend experience
## How to use it
Create new [[dotNET/API Backend/Model|Model]], for example:
``` C#
public class ServiceResponce<T>
{
    public T? Data { get; set; }
    public bool Success { get; set; } = true;
    public string Message { get; set; } = string.Empty;
}
```
And use it in services for responce