
## Methodology

- What are the available inputs?
- What are the expected outputs?
- Does not care about implementation details

## Focus

- Focuses on I/O behavior of the system
- If for any given input, the output can be predicted, then the system is considered to be correct
- Requires "test oracle" (strategy to determined whether a test passes or fails)

## Goal

- Reduce number of test cases by equivalence partitioning (grouping by equivalent behavior, e.g. inputs that pass vs inputs that fail)
    - Divide input conditions into equivalence classes
    - Choose test cases that cover all equivalence classes

## Test-case selection

- If the input is valid across a range of values...
    - The developer selects test cases from 3 equivalence classes
        - Below the range
        - Within the range
        - Above the range
- If the input is only valid if it is a member of a specific set of values...
    - The developer selects test cases from 2 equivalence classes
        - Valid discrete values
        - Invalid discrete values
- There are **no rules**, just a set of guidelines