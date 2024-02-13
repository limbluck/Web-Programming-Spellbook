To see proper enums in JSON add an attribute before a model class
``` C#
[JsonConverter(typeof(JsonStringEnumConverter))]
public enum Enumerable
{
    Key1 = 1,
    Key2 = 2,
    Key3 = 3
}
```