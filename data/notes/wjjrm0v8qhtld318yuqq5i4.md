
- Previously, symbol tables implemented as binary search trees
- These binary search trees had $O(\log n)$ lookups
- Instead of mapping a binary tree to an array, we can use a *hash table* to map a key to an array index directly
    - Hash tables work by passing a key to a **hash function** that maps the key to an array index

## Hash functions

- Say we want to store a key in an array with $M$ indices
    - There will be $n$ elements in the array
- The hash should encode the identity of a key
- We need to produce hashes in the range $[0, M-1]$ that are uniformily distributed
- There is a time and space tradeoff
    - If $M$ is larger, then we use more space but get $O(1)$ lookups
    - If $n$ is larger, then we use less space but get $O(n)$ lookups

## Hashing values

- If `k` is a positive integer within the bounds, it can simply be hashed as itself
    - Otherwise, a modulo operation can be used, e.g. `k % M`
- If `k` is a floating point number, it can be hashed as `round(k * M)`
- If `k` is a string, it can be hashed by adding the ASCII values of each character in the string
    - This is a very simple hash function, and is only effective for small strings
- If `k` is some other type, it can be hashed by mixing up a combination of the memory address, type, and other characteristics of `k`
    - In Java, this can be provided by the `Object.hashCode()` method

## Requirements for a good hash functions

- Hash functions should produce values that are...
    - Consistent
    - Efficient to compute (no more than $O(n)$)
    - Uniformly distributed

## Separate chaining

- Hash functions should rarely produce collisions, but if they do, there are many ways to resolve them
- The most common way to resolve collisions is called **chaining**
    - Chaining is a technique where multiple values can be stored at an array index
    - Some kind of linked list or tree structure is used to store the values and original keys
    - When attempting to access a value with collision, the collection is traversed (generally via [[ser222.hash-table.linear-probing]]) until the key is found
    - If using linked lists, the first value will retain $O(1)$ lookups, making it ideal for most cases
    - ![](/assets/images/2022-04-04-10-55-37.png)

## Chaining implementation

- Hash
    - Mask out the sign bit
    - Apply a module operation to the result
    - ```python
    def hash(key: int, m: int) -> int:
        return abs(key) % (m - 1) # can also be done using '(key & 0x7fffffff) % (m - 1)'
    ```
- Get
    - Gets an element to the collection by hashing the key
    - ```python
    def get(key: int, array: List[Any]) -> Any:
        values = array[hash(key, len(array))]
        values.get(key)
    ``` 
- Put
    - Similar to get, but instead of returning the value, the value is added to the collection
    - ```python
    def put(key: int, array: List[Any]) -> None:
        values = array[hash(key, len(array))]
        values.put(key, value)
    ```

## Performance

- Hash tables should have a performance of
    - $~N/2M$ search operations
    - $~N/M$ insert operations
- Hash tables can have $\Omega(1)$ search and inserts assuming no collisions