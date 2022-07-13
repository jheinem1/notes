
- Suppose there was an array of size `M`, where `M` is at least as big as `n`
- At each position, there is a key-value pair
- When inserting or searching an element, a hash function is used to map the key to an array index
- If that index is empty, use it, otherwise, keep looking for an empty index
- Essentially, instead of storing the key-value pairs in linked lists, we directly store all key-value pairs in the array
    - This works best for ordered data, but can be used for unordered data as well
- The main cost of linear probing is that inserts are $O(n)$ due to the need to resize the array when it is full rather than relying on the $O(1)$ inserts of linked lists