# Dapper
## What is it
- [GitHub - DapperLib/Dapper: Dapper - a simple object mapper for .Net](https://github.com/DapperLib/Dapper)
Dapper is a NuGet library that you can add in to your project that will enhance your ADO.NET connections via extension methods on your `DbConnection` instance. This provides a simple and efficient API for invoking SQL, with support for both synchronous and asynchronous data access, and allows both buffered and non-buffered queries.
## Key feature:
Execute sample queries from .NET:
```C#
// insert/update/delete etc - returns number of affected rows
var count  = connection.Execute(sql [, args]);

// multi-row query
IEnumerable<T> rows = connection.Query<T>(sql [, args]);

// single-row query ({Single|First}[OrDefault])
T row = connection.QuerySingle<T>(sql [, args]);
```
## Required packages:
- Dapper
- System.Data.SqlClient
## Connect with SQL
Sample connection string:
``` JSON
"ConnectionStrings": {
	"DefaultConnection" : "Server=.\\SQLEXPRESS; Database=Purity_DB; Trusted_Connection=true, TrustServerCertificate=true; Integrated Security=true; Encrypt=false"
}
```
Connect:
``` C#
// Inject:
private readonly IConfiguration _config;
public constructor(IConfiguration config)
{
	_config = config;
}
// Use:
using var connection = new SqlConnection(_config.GetConnectionString("DefaultConnection"));
```
