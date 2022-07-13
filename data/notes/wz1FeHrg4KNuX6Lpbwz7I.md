
A special case of association denoting a "conists-of" hierarchy.

The aggregate is the parent class, and the components are children classes

```mermaid
classDiagram
    ExhaustSystem o-- Muffler
    ExhaustSystem o-- Tailpipe
    Muffler : number diameter
    Tailpipe : number diameter
```
^main
## Composition
A string form of aggregation denoted by a solid diamond.

The lifetime of component instances are controlled by the aggregate (they cannot exist independently).

```mermaid
classDiagram
    TicketMachine *-- "3" ZoneButton
```