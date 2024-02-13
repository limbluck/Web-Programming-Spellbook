# Data types
## Text
|  | Unicode (International) | non-Unicode |
| ---- | ---- | ---- |
| Fixed length | nchar | char |
| Variable length | nvarchar | varchar |
nvarchar(4000)
varchar(8000)
nvarchar(max) - up to 2GB
text and ntext are deprecated
## Exact numbers
| Data type | Numbers | C# Data type |
| ---- | ---- | ---- |
| int | +/- 2 billion | int |
| smallint | 32,768 to 32,767 | short |
| tinyint | 0 to 255 | byte |
| bigint | +/- 2^63 |  |
| money | +/- 922,337,203,685,477.5808 | long |
| smallmoney | +/- 214,748.3648 |  |
| decimal(p, s) or numeric (p, s) | fixed precision and scale |  |
max of decimal(9, 2) or numeric (9, 2) is 9999999.99
## Approximate numbers
| Data type | Numbers |
| ---- | ---- |
| float(n) |  |
| real |  |
## Date
| Data type | Numbers |
| ---- | ---- |
| date | Only date |
| time | Only time |
| datetime | Date and time |
| datetime2 | Recommended |
| datetimeoffset | Offset of date and time |
## Other
| Data type | Numbers |
| ---- | ---- |
| binary() | fixed length binary |
| varbinary() | variable length binary |
| bit | boolean |
| xml | xml data |
| uniqueidentifier | 16 digits unique ID (create by newid() function) |
