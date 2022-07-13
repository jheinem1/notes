
## Compared to heaps

- Unlike [[binary trees|ser222.binary-tree]] and [[heaps|ser222.heap]], binary search trees *must* bee complete
- Binary search trees are more restrictive than heaps

## Concept

- A [[binary tree|ser222.binary-tree]] is a tree where each node has at most two children
- A binary *search* tree is a binary tree where each node's left child has a key that is less than the parent, and the right child has a key that is greater than the parent
- ![](/assets/images/2022-03-23-10-48-39.png)

### Recursive definition

- A node is the root of a binary search tree if...
    - The left child has a key less than the parent, and the child is the root of a binary search tree
    - The right child has a key greater than the parent, and the child is the root of a binary search tree
## Traversing

The three main algorithms for traversing a binary search tree are...

### Pre-order traversal

1. Visit the root node
2. Traverse the left subtree
3. Traverse the right subtree

```java
public void preOrder(Node root) {
    if (root == null) return;
    System.out.println(root.key);
    preOrder(root.left);
    preOrder(root.right);
}
```

### In-order traversal

1. Traverse the left subtree
2. Visit the root node
3. Traverse the right subtree

```java
public void inOrder(Node root) {
    if (root == null) return;
    inOrder(root.left);
    System.out.println(root.key);
    inOrder(root.right);
}
```

### Post-order traversal

1. Traverse the left subtree
2. Traverse the right subtree
3. Visit the root node

```java
public void postOrder(Node root) {
    if (root == null) return;
    postOrder(root.left);
    postOrder(root.right);
    System.out.println(root.key);
}
```

## Inserting

See the [[ser222.symbol-table]] [[get|ser222.symbol-table#Get value implementation]] and [[put|ser222.symbol-table#Put value implementation]] for more details.

## Layout

- Three cases for tree layout
    - Worst case
        - The tree is completely unbalanced
        - $O(n)$ search time
        - ![](/assets/images/2022-03-23-11-19-46.png)
    - Typical case
        - Somewhat balanced
        - ![](/assets/images/2022-03-23-11-20-25.png)
    - Best case
        - Perfectly balanced, as all things should be
        - $O(\log n)$ search time
        ![](/assets/images/2022-03-23-11-20-57.png)