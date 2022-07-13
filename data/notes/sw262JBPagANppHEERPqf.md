## Overview
- Abstract data type (ADT): a datatype that is represented in terms
of operations, and whose internal representation is hidden.
- Naturally defined by objects – but adds emphasis on abstraction.
- A user of an ADT is meant to be isolated from its implementation
(e.g., internal presentation). They should care only for the
behavior that is exposed (via an API).
## Dynamic View
- Rather than relying on a class/object view, ADTs can be represented in terms of operations happening over types
    - add: Point2D ⨯ Point2D → Point2D
    - subtract: Point2D ⨯ Point2D → Point2D
    - getX: Point2D → double
    - getDistance: Point2D ⨯ Point2D → double
    - equal: Point2D ⨯ Point2D → boolean
- ADTs have two basic operations
    - Transformations
    - Information exstraction
## Usage
Since ADTs are implemented using classes, they use all operations allowed for classes, e.g.
- Creation `LinkedStack stack = new LinkedStack();`
- Invocation `stack.push(5);`
- Copy Behavior `=`
## ADTs VS Classes
- ADTs are differnet from classes because of abstraction
    - An ADT does not expose internal representations
    - Classes have no such restrictions
    - Purely a design difference (not enforced by syntax)
- ADTs are **not** abstract classes
