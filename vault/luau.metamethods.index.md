---
id: jzysbl25j6w405zgishuyts
title: __index
desc: ''
updated: 1655765828778
created: 1655765797284
---

```Lua
__index<T>(self: T, key: unknown): typeof T[key]
```
OR
```Lua
__index: table
```
Fires when `self[key]` is indexed, if `self[key]` is nil. Can also be set to a table, in which case that table will be indexed.