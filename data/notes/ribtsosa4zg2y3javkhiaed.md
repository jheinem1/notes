
```Lua
__lt<T>(self: T, value: T): boolean
```
The `<` less than operator; **NOTE**: Using the `>=` greater than or equal to operator will invoke this metamethod and return the opposite of what this returns, as greater than or equal to is the same as not less than. Requires two values with the same metatable and basic type (table/userdata/etc.); does not work with a table and another random table, or with a userdata and a table.