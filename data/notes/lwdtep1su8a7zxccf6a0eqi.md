
Given a graph with the vertices `a` pointing to `b`, how can we ensure that when traversing, `a` is always visited before `b`?

![](/assets/images/2022-04-20-11-07-23.png)

## Topological sorts

To solve this, a graph should be sorted with a [[ser222.directed-graphs.topological-sort]] before traversal.