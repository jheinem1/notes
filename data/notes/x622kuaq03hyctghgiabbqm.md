
## When unit tests are written

- Traditionally, after the source code is written
- In [[ser216.software-development-lifecycle.agile-method.extreme-programming]] & [[ser216.test-driven-development]], before the source code is written

## Types of unit tests

- Static testing (compile-time)
    - [[ser216.unit-testing.static-analysis]]
    - Code review
        - Walk-through (informal)
        - Inspection (formal)
    - Automated tools
        - Check for syntax & semantic errors
        - Check for departure from standards
- Dynamic testing (runtime)
    - [[ser216.unit-testing.black-box-testing]]
    - [[ser216.unit-testing.white-box-testing]]

## Heuristics

1. Create tests when object design is completed
    - Black box: test the functional model
    - White box: test the dynamic model
2. Develop test-cases
    - Find effective number of test-cases
3. Cross-check test cases to eliminate duplicates
4. Desk-check source code
5. Create a test harness
    - e.g. test drivers and stubs
6. Describe the test oracle
    - Often the result of the first successful test
7. Execute test cases
8. Compare results of the test with the oracle
    - If possible, automate