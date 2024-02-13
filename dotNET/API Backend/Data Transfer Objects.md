# Data Transfer Objects
## What is it
Data types created to use in data transfer cases, when we don't want to respond with original object with all of it's properties 
## How to use it
Create a DTO class 
``` C#
public class DTO
{
    public int property1 { get; set; }
    public int property2 { get; set; }
    public int property3 { get; set; }
}
```
[[dotNET/AutoMapper|Map]] object to the dto class