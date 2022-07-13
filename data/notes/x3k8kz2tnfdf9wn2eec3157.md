
## Metatables

A metatable is a table full of metamethods which overload the functionality of existing types in Luau. Under the hood, every operator in Luau is essentially a function call. Metatables are primarily used to add functionality to [[luau.types.userdata]], which can easily be implemented in C++.

## Metamethods

Metamethods are functions within metatables such as [[luau.metamethods.index]] and [[luau.metamethods.add]] that define the behavior of operators in Luau acting on a given type.

## Interaction

[[luau.globals.setmetatable]] and [[luau.globals.getmetatable]] are primarily used to interact with metatables.