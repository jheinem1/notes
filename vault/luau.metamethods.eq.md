---
id: 88rjpwi9w6s86d79hnz0701
title: __eq
desc: ''
updated: 1655765753137
created: 1655765744062
---

```Lua
__eq<T>(self: T, value: T): boolean
```
The `==` equal to operator. Requires two values with the same metatable and basic type (table/userdata/etc.); does not work with a table and another random table, or with a userdata and a table.