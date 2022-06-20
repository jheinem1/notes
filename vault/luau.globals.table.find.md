---
id: cg8fys47kw18v3ltpfj3e31
title: table.find
desc: ''
updated: 1655768171496
created: 1655765559594
---

```lua
table.find<T extends table>(haystack: T, needle: unknown, init: number): T extends Array ? number : unknown
```

Within the given array-like table haystack, find the first occurrence of value needle, starting from index `init` or the beginning if not provided. If the value is not found, `nil` is returned.

A linear search algorithm is performed.

## Examples
```Lua
local t = {"a", "b", "c", "d", "e"}
print(table.find(t, "d")) --> 4
print(table.find(t, "z")) --> nil, because z is not in the table
print(table.find(t, "b", 3)) --> nil, because b appears before index 3
```