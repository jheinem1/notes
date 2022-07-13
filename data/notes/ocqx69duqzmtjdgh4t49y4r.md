
- Tests the top layer first (without any subsystems)
    - Stubs are required
- Then, combines all subsystem called by the tested subsystem and test the resulting collection
- Repeat until all subsystems are included

![](/assets/images/2022-04-19-14-21-21.png)

## Advantages

- Test cases defined in terms of functionality of the system
- Does not require drivers

## Disadvantages

- Stubs can be difficult to implement
- Large amounts of stubs are required
- Some interfaces cannot be tested separately