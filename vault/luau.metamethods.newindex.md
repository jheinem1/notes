---
id: exgc8uwytsjoguk6w5chqyx
title: __newindex
desc: ''
updated: 1655766192074
created: 1655766164750
---

```Lua
__newindex<T>(self: T, key: unknown, value: unknown): nil
```
OR
```Lua
__newindex: table
```
Fires when `table[index]` tries to be set (`table[index] = value`), if `table[index]` is `nil`. Can also be set to a table, in which case that table will be indexed.