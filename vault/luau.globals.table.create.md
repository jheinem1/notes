---
id: 1y5h9mf7g9a2wbcwgsuvyzd
title: Create
desc: ''
updated: 1655768057451
created: 1655765503701
---

```Lua
table.create<T>(count: number, value: T): Array<T>
```

Given an array where all elements are strings or numbers, returns the string `t[i] … sep … t[i+1] … sep … t[j]`. The default value for sep is an empty string, the default for `i` is `1`, and the default for `j` is `#t`. If `i` is greater than `j`, returns the empty string.