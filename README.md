# Lab 9

!(example.pdf)[Train crossing state diagram]

## Invarients
- There is power
- The trains operate within a certain speed limit, such that they can't cross the distance between the sensor and the crossing before the elapsed time.
- The motor for the arms works.

 ## Counter Example
 -  If there are two trains on the track, such that one train leaves triggering arms up while the other train remains on the tracks the system will be in an unsafe state.
