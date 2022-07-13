
- In Functional Decomposition, the system is decomposed into models
- Each model is a major processing step
- Modules can be decomposed into smaller modules.

```mermaid
flowchart TD
    sf(System Function) --- ri0(Read Input)
    sf --- tf0(Transform)
    sf --- po0(Produce Output)
    ri0 --- ri1(Read Input)
    ri0 --- tf1(Transform)
    ri0 --- po1(Produce Output)
    ri1 --- o0[(...)]
    tf1 --- o1[(...)]
    po1 --- o2[(...)]
    tf0 --- o3[(...)]
    po0 --- o4[(...)]
```

...which eventually leads to something like

```mermaid
flowchart TD
    o0[(...)] --- l(LoadR10)
    o0 --- a(Add R1, R10)
```

## Why is Functional Decomposition Important?

- Functionality is spread across the system
- Maintainer must understand the whole system to make a single change
- Consequences...
  - Code that is hard to understand
  - Code that is complex and impossible to maintain
- Example: [[PowerPoint Autoshapes|ser216.introduction.decomposition.functional.autoshape]]
