
```Java
...
    public boolean isEmpty() { // [1]
        return n == 0;
    }
    public Item pop() { // [2]
        if (isEmpty())
            throw new ...
        return data[--n];
    }
    public void push(Item item) { // [3]
        if (data.length == n)
            resize(); // doubles the size of the array
        data[n++] = item;
    }
    private void resize() {
        data = Arrays.copyOf(data, data.length * 2);
    }
...
```
1. What is the Big-Oh of `isEmpty()`?
    - `O(1)`
2. What is the Big-Oh of `pop()`?
    - `O(1)`
3. What is the Big-Oh of `push()`?
    - `O(n)`, because the worst case involve array resizing (which performs a deep copy of the array)

What if we wanted to implement a `push()` and `pop()` that are both `O(1)`? We need a new data structure such as a [[ser222.linked-list]].