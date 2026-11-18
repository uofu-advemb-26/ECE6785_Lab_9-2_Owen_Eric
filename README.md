# Lab 9

!(example.pdf)[Train crossing state diagram]
![Train Crossing State Diagram](example.pdf)

## Invariants
- There is power.
- The trains operate within a certain speed limit, such that they can't cross the distance between the sensor and the crossing before the elapsed time.
- The motor for the arms works.
- Only one input can happen at a time


## Varying invariants
 -  If there are two trains on the track, such that one train leaves triggering arms up while the other train remains on the tracks the system will be in an unsafe state.

## Check your work

### Owen's Train Crossing Diagram
![Owen's train diagram](owen_train_diagram.png)


## Prove It

| number | arms_down | alarm_on | northbound_present | southbound_present | north_approach | south_approach | north_depart | south_depart | ringing | safety_hazard |
|--------|-----------|----------|--------------------|--------------------|----------------|----------------|--------------|--------------|---------|---------------|
| 0      | 0         | 0        | 0                  | 0                  |        14      |       13       |     0        |      0       |   ?     |      0        |
| 1      | 0         | 0        | 0                  | 1                  |        15      |       13       |     13       |      0       |   ?     |      1        |
| 2      | 0         | 0        | 1                  | 0                  |        14      |       15       |     0        |      14      |   ?     |      1        |
| 3      | 0         | 0        | 1                  | 1                  |        15      |       15       |     13       |      14      |   ?     |      2        |
| 4      | 0         | 1        | 0                  | 0                  |        14      |       13       |     0        |      0       |   ?     |      0        |
| 5      | 0         | 1        | 0                  | 1                  |        15      |       13       |     13       |      0       |   ?     |      1        |
| 6      | 0         | 1        | 1                  | 0                  |        14      |       15       |     0        |      14      |   ?     |      1        |
| 7      | 0         | 1        | 1                  | 1                  |        15      |       15       |     13       |      14      |   ?     |      2        |
| 8      | 1         | 0        | 0                  | 0                  |        14      |       13       |     0        |      0       |   ?     |      1        |
| 9      | 1         | 0        | 0                  | 1                  |        15      |       13       |     13       |      0       |   ?     |      1        |
| 10     | 1         | 0        | 1                  | 0                  |        14      |       15       |     0        |      14      |   ?     |      1        |
| 11     | 1         | 0        | 1                  | 1                  |        15      |       15       |     13       |      14      |   ?     |      1        |
| 12     | 1         | 1        | 0                  | 0                  |        14      |       13       |     0        |      0       |   ?     |      0        |
| 13     | 1         | 1        | 0                  | 1                  |        15      |       13       |     13       |      0       |   ?     |      0        |
| 14     | 1         | 1        | 1                  | 0                  |        14      |       15       |     0        |      14      |   ?     |      0        |
| 15     | 1         | 1        | 1                  | 1                  |        15      |       15       |     13       |      14      |   ?     |      0        |

| number | invariant                                                 |
|--------|-----------------------------------------------------------|
| 16     | A train must depart before the next enters the same track |
| 17     | There is Power                                            |
| 18     | The arms and alarms move instantly                        |
| 19     | Only one input happens at a time                          |

## Specification vs.implementation







