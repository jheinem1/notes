
For small-to-medium-sized teams developing software with vague or rapidly changing requirements.

^when-to-use

Coding is the key activity throughout a software project.

- Communication among teammates is done with code
- Life cycle and behavior of complex objects defined in test cases (also in code)

## XP is "extreme" because...

Commonsense practices are taken to extreme levels:

- If **code reviews** are good, review code _all the time_ (pair programming)
- If **testing** is good, everybody will test _all the time_
- If **simplicity** is good, keep the system in the simplest design that supports current functionality
- If **design** is good, everybody will design (refactor) daily
  - There are no formal design documents (UML or otherwise)
- If **architecture** is important, everybody will work at defining and refining the architecture
- If **integration testing** is important, build and integrate test several times a day
- If **short iterations** are good, make iterations as short as possible (hours rather than weeks)

## Principles

1. Planning game
   - Determine scope of the next release by combining business priorities and technical estimates
2. Small releases
   - Put a simple system into production
   - Then release new versions in short cycles
3. Metaphor
   - All development is guided by a simple shared story of how the system works
4. Simple design
   - System is designed as simply as possible
   - Extra complexity is removed as soon as discovered
5. Testing
   - Programmers continuously write unit tests
   - Customers write tests for features
6. Refactoring
   - Programmers continuously restructure the system without changing behavior
7. Pair-programming
   - All production code is written with two programmers at one machine
8. Collective ownership
   - Anyone can change any code anywhere at any time
9. Continuous integration
   - Integrate and build the system every time a task is completed
10. 40-hour week
    - Work no more than 40 hours a week as a rule
    - This is not closely followed
11. On-site customer
    - A user is on the time and available full-time to answer questions
12. Coding standards
    - Programmers write all code in accordance with rules emphasizing communications through the code
