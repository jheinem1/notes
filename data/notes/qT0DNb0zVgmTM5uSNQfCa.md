
Structural things are used to define the static parts of models, representing physical and conceptual elements.

## Class
Represents a set of objects having similar responsibilities

|Class|
|-|
|Attributes|
|Operations|

## Interface
Defines a set of operations which specify the responsiblity of the class

|Interface|
|-|
||

## Collaboration
Defines an interaction between elements.
```mermaid
flowchart TD
    A[window : UserInterface] -->|makeReservation| B[myHotel : Hotel];
```
## Use Case
A set of actions performed by a system for a specific goal.
```mermaid
flowchart LR
    id1([Use case])
```
## Component
A physical part of a system
```mermaid
flowchart TD
    A[Component];
```
## Node
A physical element that exists at run-time
```mermaid
flowchart TD
    A[Node];
```
An edge between two notes denotes a relationship between the corresponding entities.