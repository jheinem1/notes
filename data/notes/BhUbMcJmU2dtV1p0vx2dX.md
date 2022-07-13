
Describe the functional behavior of the system as seen by the user
- Used during requirements elicitation and analysis to represent external behavior
- An Actor represents a role
```mermaid
sequenceDiagram
    actor Passenger
```
- A use-case represents a class of functionality provided by the system
- The textual use-case description consists of 6 parts...
    1. Unique name
    2. Participating actors
    3. Entry conditions
    4. Exit conditions
    5. Flow of events
    6. Special Requirements
## <<extends\>> relationship
- Used to extend use-cases
- ![](/assets/images/2022-01-20-14-29-15.png)
## <<includes\>> relationship
- Represents functionality in more than one use-case
- ![](/assets/images/2022-01-20-14-30-14.png)