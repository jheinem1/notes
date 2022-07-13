
- In most cases, unchecked exceptions reflect programming logic errors that are not recoverable, e.g.
    - `NullPointerException` is thrown if you access an object through a reference variable before an object is assigned to it
    - `IndexOutOfBoundsException` is thrown if you access an element in an array outside the bounds of the array
- These are logic errors that should be corrected in the program
- Unchecked exceptions can occur anywhere in a program
- To avoid cumbersome overuse of try-catch blocks, Java does not mandate you write code to catch unchecked exceptions