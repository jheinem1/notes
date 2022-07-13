
## Proof of termination

- Shows that an algorithm always terminates
- First step towards producing something useful
    - Otherwise program could be infinite loop
- Typically performed by determining a progress metric, then showing an algorithm "moves along" the metric

### Example - Proving 'swim' terminates

```python
def swim(self, k: int):
    while (k > 1 and (parent := k / 2) < k)
        exch(k, (k := parent))
```

We can infer that the only place where the algorithm could not terminate is when the `while` loop is entered.

Because `k` is constantly being set to `parent`, the loop can terminate as the value of `parent` will eventually reach either `1`, or less than `1` since `parent` is set to `k / 2` each iteration. Additionally, since `k` and `parent` are both integers, `1 / 2` will round down to `0` rather than up to `1`.

## Proof of correctness

- Shows that an algorithm always performs in a certain way, or acts according to certain constraints
- If we have proof of correctess, that assets the algorithm is correct
    - The remaining question would be, "is the algorithm fast enough?"
- Typically performed by analyzing the way the algorithm transforms data to argue the output will always have certain properties

### Example - Proving 'swim' is correct

```python
def swim(self, k: int):
    while (k > 1 and (parent := k / 2) < k)
        exch(k, (k := parent))
```

> Let `k` be the node that will be swim'ed. If `k` is a node already in its proper position then `less(parent(k), k)` will always be `False`, and no code will be run.

From this, we can infer that the result is correct because we know that `parent(k)` should always be less than `k` in an ordered max heap.

### Metric 1

Using the metric defined earlier...

> The ability of the algorithm to process a heap-sorted array with at most one node which violates the heap rule and produce a heap-sorted array with no violations of the maximum heap rule. The array must contain a complete tree at all times.

#### Case 1

- Tree does not contain node with value
- In step 1, we loop over tan element and check its contents
- No changes are made to `N`, `keys`, or `value`, so after that step, the data will be heap-ordered
- If there is no node to update, the algorithm will terminate

#### Case 2

- Tree contains node with value
- We defer to the mechanisms for `swim` and `sink` which are already known to result in a heap-ordered array
- Both functions will terminate if there is no work to do
- The `if`-statements evaluate the case of being out of order with `parent` or `children,` and follows the formula as defined

## Proof of efficiency

- The metric we defined earlier was

> M1
> For a cost metric, we will use the number of lines run as a measure of computational time needed for particular design.

- Since we are working with an algorithm, we want to show that our algorithm is at least as fast as any other

### Metric 2

- Per `K`, insert takes $O(\log n)$
    - Thus, the best we can get is $O(\log n)$