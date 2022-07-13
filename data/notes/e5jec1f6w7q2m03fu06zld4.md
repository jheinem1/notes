
## Pseudocode

- The purpose of pseudocode is to **clearly** express an algorithm
    - There cannot be ambiguity
- Pseudocode cannot be used to hide important details
    - It's only fair to reference an undefined function when it does not add more ambiguity, e.g. calling `distance(x1, y1, x2, y2)` is fine, but calling `has_deviation(original_image, new_image)` is not

### Examples

```java
public void insert(Key v) { 
    pq[++N] = v;
    swim(N);
}

private void swim(int k) {
    while (k > 1 && less(k / 2, k)) {
        exch(k, k / 2);
        k = k / 2;
    }
}

void insert(Key v) {
    pq[++N] = v;
    swim(N);
}

void swim(int k) {
    while (k > 1 && less(k / 2, k)) {
        exch(k, k / 2);
        k = k / 2;
    }
}
```

Pseudocode does not need to compile, however it is helpful to use a specific language's syntax to make it easier to read. Python is often used because it closely resembles plain English and generally produces relatively readable and concise code.

## K

- "K" stands for knowledge and is the symbol we will use to refer to the set of information which is known to be true
    - In a class, "K" is typically provided as a working document
- The purpose of "K" is to ensure a design is well-founded
- "K" can serve as a safe place to put generic definitions
    - "K" = [[Definitions|ser222.algorithms.adj.analysis#Definitions]]

## Decomposition

Since we have a good understanding of the [[problem|ser222.algorithms.adj.problem-statement]], we can attempt to break it into steps (and pseudocode).

1. Find target key/value
2. If needed, adjust position of target key/value

```python
def update(value: Value, new_priority: Key):
    idx: int | None = None
    
    # Step 1: Find target key/value
    for i in range(0, n - 1):
        if values[i] == value:
            idx = i
            break
    
    if idx == None:
        return

    # Step 2: Adjust position of target key/value
    keys[idx] = new_priority
    if less(keys[idx / 2], new_priority):
        swim(idx)
    elif less(new_priority, max(keys[2 * idx], keys[2 * idx + 1])):
        sink(idx)
```