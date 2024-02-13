To allow Cross Origin Resource Sharing use next in Program.cs:
``` C#
builder.Services.AddCors(options =>
{
    options.AddPolicy(name: AllowOrigin,
                      policy =>
                      {
                          policy.WithOrigins("origin url");

                          policy.WithHeaders("access-control-allow-origin");
                          policy.WithHeaders("content-type");
                      });
});
app.UseCors(MyAllowSpecificOrigins);
```