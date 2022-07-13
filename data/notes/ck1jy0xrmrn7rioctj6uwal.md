
Analysis is the stage at which the problem is defined.

For example...

- *What is meant by "updating" a Priority Queue?*
- *Are any (reasonable) assumptions needed?*
- *How is data represented?*

## Problem statement

For the purposes of demonstration, we will use a sample design problem.

![[ser222.algorithms.adj.problem-statement]]

## Understanding the problem

Under specified aspects:

- *Is this a max or min PQ?*
    - This is a max PQ
- *What implementation do we need to support?*
    - Sedgewick's

## Doing examples by hand

![](/assets/images/2022-03-16-11-05-43.png)

Before you begin writing code, ensure you know what exactly you are trying to solve.

## Definitions

> Design an efficient algorithm to update the priority of an entry inside a priority queue.

There is ambiguity in this statement, so we will make assumptions about the problem.

### Assumptions

- The priority queue is a max priority queue
- The specific implementation is Sedgewick's
- The algorithm will assume that it operates over a valid PQ and produces a valid PQ

### Definitions

1. [[ser222.binary-tree]]
2. [[ser222.complete-binary-tree]]
3. [[ser222.heap]]
4. [[Heap-ordered Array|ser222.binary-tree#Mapping to an array]]
5. [[ser222.sorting.priority-queue]]

### Pseudocode

```python
n: int # number of elements in the PQ
keys: [Key] # array of keys containing 'n' elements
values: [Value] # array of values containing 'n' elements

def update(value: Value, new_priority: Key):
    """
    Changes the priority of the node with the given value to the new priority.
    
    Parameters
    ----------
    value: Value
        The value of the node to update
    new_priority: Key
        The new priority of the node
    """
```

## Metrics

> Design an efficient algorithm to update the priority of an entry inside a priority queue.

Need to find what is important, distill it, and define it.

- M1: The ability of the algorithm to process a heap sorted array with at most one node which violates the heap rule and produce a heap-sorted array with no violations of the maximum heap rule. The array must contain a complete tree at all times
- M2: The efficiency of the algorithm. In this case, we can use the number of lines run as a measure of computational time.

## Conclusion

We've...

- Understood the problem
- Created a sound technical context for the problem
- Determined what makes a good solution