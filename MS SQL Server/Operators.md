# Operators
## Basic operators
| Operator | Description |
| ---- | ---- |
| = | Equal |
| != | Not equal |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal |
| <= | Less than or equal |
| AND | and |
| OR | or |
## LIKE
Search for a pattern
% - any string of any characters
_ - any character
\[  \] - Any single character within the specified range `[a-f]` or set `[abcdef]`.
\[^\] - Any single character not within the specified range `[^a-f]` or set `[^abcdef]`.
## IN
To specify multiple possible values for a column
If the value of _test_expression_ is equal to any value returned by _subquery_ or is equal to any _expression_ from the comma-separated list, the result value is TRUE; otherwise, the result value is FALSE.
``` SQL
test_expression [ NOT ] IN ( subquery | expression [ ,...n ] )
```
