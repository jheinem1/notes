---
id: 9iboxkp4dqmvzg6vsgjgbdf
title: table.sort
desc: ''
updated: 1655769067767
created: 1655768901131
---

```lua
table.sort(t: Array, cmp: ((a: unknown, b: unknown) => boolean)?)
```

If no `cmp` function is provided, sorts an array of numbers using the equivalent of

```lua
function(a, b)
    return a < b
end
```

. If `cmp` is provided, it is used to compare the elements.