# Functions
## String
| Function | Description |
| ---- | ---- |
| len(str) | Returns the length of a string |
| left(str, num) | Extracts a number of characters from a string (starting from left) |
| right(str, num) | Extracts a number of characters from a string (starting from right) |
| lower(str) | Converts a string to lower-case |
| upper(str) | Converts a string to upper-case |
| trim(str) | Removes leading and trailing spaces (or other specified characters) from a string |
| ltrim(str) | Removes leading spaces from a string |
| rtrim(str) | Removes trailing spaces from a string |
| patindex(pat, str) | Returns the position of a pattern in a string |
| replace(str, old, new) | Replaces all occurrences of a substring within a string, with a new substring |
| replicate(str, num) | Repeats a string a specified number of times |
| reverse(str) | Reverses a string and returns the result |
| str(num) | Returns a number as string |
| stuff(str, pos, num, newstr) | Deletes a part of a string and then inserts another part into the string, starting at a specified position |
| substring(str, pos, num) | Extracts some characters from a string |
## Math
| Function | Description |
| ---- | ---- |
| abs(num) | Returns the absolute value of a number |
| avg(nums) | Returns the average value of an expression |
| round(num) | Rounds a number to a specified number of decimal places |
| ceiling(num) | Returns the smallest integer value that is >= a number |
| floor(num) | Returns the largest integer value that is <= to a number |
| count(objs) | Returns the number of records returned by a select query |
| max(nums) | Returns the maximum value in a set of values |
| min(nums) | Returns the minimum value in a set of values |
| power(num, pow) | Returns the value of a number raised to the power of another number |
| rand() | Returns a random number |
| sign(num) | Returns the sign of a number |
| sum(nums) | Calculates the sum of a set of values |
## Date
| Function | Description |
| ---- | ---- |
| dateadd(interval, number, date) | Adds a time/date interval to a date and then returns the date |
| datediff(interval, number, date) | Returns the difference between two dates |
| datefromparts(year, month, day) | Returns a date from the specified parts (year, month, and day values) |
| datename(interval, date) | Returns a specified part of a date (as string) |
| datepart(interval, date) | Returns a specified part of a date (as integer) |
| getdate() | Returns the current database system date and time |
| day(date) | Returns the day of the month for a specified date |
| month(date) | Returns the month part for a specified date (a number from 1 to 12) |
| year(date) | Returns the year part for a specified date |
| isdate(val) | Checks an expression and returns 1 if it is a valid date, otherwise 0 |
| sysdatetime() | Returns the date and time of the SQL Server |
## Advanced
| Function | Description |
| ---- | ---- |
| convert(DataType, value) | Converts a value (of any type) into a specified datatype. |
