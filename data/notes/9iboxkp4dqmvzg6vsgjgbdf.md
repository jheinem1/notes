
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