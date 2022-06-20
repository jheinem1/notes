---
id: 7rtbigt1xgesltqm8afze5y
title: __tostring
desc: ''
updated: 1655766259555
created: 1655766241305
---

```Lua
__tostring<T>(self: T): string
```
Fired when `tostring` is called on the table. Also fired when encoding tables to JSON (something to note because table keys can have objects with custom metatables.