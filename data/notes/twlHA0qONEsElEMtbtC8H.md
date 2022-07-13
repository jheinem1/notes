
Immutability is an OO concept where the internal state of objects cannot change after instantiation (all fields are final). Performing any operations on the object will simply return a new object that reflects the changes.

## Pros:
- Reduces undefined behavior in programs
- Eliminates the possibility of accidentally modifying objects being used somewhere else
## Cons:
- Can significantly increase memory usage
- Comes at a performance cost in heavy tasks as the garbage collector may have to work harder

```TypeScript
class Number {
    constructor(public n: number) {}
    add(n: Number) {
        return new Number(this.n + n.n)
    }
}
```