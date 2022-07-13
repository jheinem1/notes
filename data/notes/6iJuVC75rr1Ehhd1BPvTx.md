
- If there is a small issue with one of the shapes, it is incredibly difficult to fix
- Adding a new shape generally requires code reuse, also requiring a good understanding of the system

```mermaid
flowchart TD
  Autoshape(Autoshape) --- Mouse(Mouse Click)
  Autoshape --- Change(Change)
  Autoshape --- Draw(Draw)
  Change --- ChangeR(Change Rectangle)
  Change --- ChangeO(Change Oval)
  Change --- ChangeC(Change Circle)
  Draw --- DrawR(Draw Rectangle)
  Draw --- DrawO(Draw Oval)
  Draw --- DrawC(Draw Circle)
```

Effectively you keep breaking down high level functions into smaller functions until you reach the actual code.
