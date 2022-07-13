
```lua
table.insert(t: table, pos: unknown, value: unknown)
```

Inserts the value `value` into the table `t` at the index or key `pos`. If `pos` is an index in the array portion of the table, all values at and after `pos` are shifted by one index to the right. If `pos` is a key in the table, the value at that key is overwritten.