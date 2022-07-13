
```lua
table.remove(t: table, pos: unknown): unknown
```

Removes the element at the position `pos` from the table `t`. If `pos` is in the array portion of the table, all elements after `pos` are shifted down. If `pos` is in the hash portion of the table, the key-value pair is