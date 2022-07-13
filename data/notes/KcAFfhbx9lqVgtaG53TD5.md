
## State diagram of a microwave oven
![](/assets/images/2022-01-25-14-28-22.png)
## States for the microwave oven
| State      | Description                                                                                                                                                                                                                     |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Waiting    | The oven is waiting for input. The display shows the current time.                                                                                                                                                              |
| Half Power | The oven power is set to 300 watts. The display shows ‘Half power’.                                                                                                                                                             |
| Full Power | The oven power is set to 600 watts. The display shows ‘Full power’.                                                                                                                                                             |
| Set Time   | The cooking time is set to the user’s input value. The display shows the cooking time selected and is updated as the time is set.                                                                                               |
| Disabled   | Oven operation is disabled for safety. Interior oven light is on. Display shows ‘Not ready’.                                                                                                                                    |
| Enabled    | Oven operation is enabled. Interior oven light is off. Display shows ‘Ready to cook’.                                                                                                                                           |
| Operation  | Oven in operation. Interior oven light is on. Display shows the timer countdown. On completion of cooking, the buzzer is sounded for five seconds. Oven light is on. Display shows ‘Cooking complete’ while buzzer is sounding. |
## Stimuli for the microwave oven
| Stimulus    | Description                                    |
| ----------- | ---------------------------------------------- |
| Half Power  | The user has pressed the half-power button.    |
| Full Power  | The user has pressed the full-power button.    |
| Timer       | The user has pressed one of the timer buttons. |
| Number      | The user has pressed a numeric key.            |
| Door Open   | The oven door switch is not closed.            |
| Door Closed | The oven door switch is closed.                |
| Start       | The user has pressed the Start button.         |
| Cancel      | The user has pressed the Cancel button.        |
