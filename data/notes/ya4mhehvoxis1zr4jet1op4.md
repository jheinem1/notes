
- Checked exceptions can occur because of a variety of factors, however generally stem from bad inputs, e.g.
    - `ClassNotFoundException` thrown when attempting to load in a class by its string name when it does not exist
    - `IOException` signals an I/O exception of some kind has occured
- Java requires these kinds of exceptions to be handled
- These can usually be handled gracefully without terminating the program
