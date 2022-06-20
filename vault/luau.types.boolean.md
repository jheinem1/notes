---
id: aj6qdqhmbx6p1t4k1sx1q9h
title: Boolean
desc: ''
updated: 1655766798893
created: 1655766526714
---

A boolean in luau is a simple binary value that is either `true` or `false`. Booleans are not to be confused with truthy or falsy values, which are used in luau for conditionals.

## Manipulating booleans

- `not bool`: inverts the boolean
- `bool and bool`: returns `true` if both booleans are `true`
- `bool or bool`: returns `true` if either boolean is `true`

These operations also work with other types, but the result is often a truthy or falsy value rather than a boolean (with the exception of `not`).


```lua
local a = true
local b = false
local c = "hello

print(not a) -- false
print(not b) -- true
print(not c) -- false
print(a and b) -- false
print(a or b) -- true
print(a and c) -- "hello"
print(c or a) -- "hello"
print(c and a) -- true
```