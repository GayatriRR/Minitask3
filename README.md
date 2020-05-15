# Minitask3

## TASK 1: SMART RING
The idea behind this ring is to make the ring light up when worn by the user. The previous model involved a switch which would get pressed when worn that would light up the LED. Thus, it gives rise to the idea of lighting it up using touch sensors.

### Constraints:
It being a ring brings a big constraint in the form of size. Moreover, as it is going to be worn, the heating effect should be less. Current through the circuit should be maintained low to make it as safe as possible. The components also must have a sleep/low power mode to minimise the power lost while it is not being used.

### Ideation:
As the presence of an external switch is the problem with the system in the first place, we need an internal switch in the circuit which will let the LED glow when the ring is worn. To ponder on the possible solutions, we need to analyse what haappens when the ring is worn:
* The finger touches the inner part of the ring.
* The inner area of the ring is cut off from light.
* A pressure is applied on the inner surface of the ring.

| Idea | Implementation | Comments |
|-------------------|--------------------|--------------------|
| External trigger to complete the circuit when pressed | Some external component, similar to a mini-button to which can switch on the circuit when pressed. | Simple. But can cause discomfort. |
| Touch sensor | A [TTP223](https://datasheet.lcsc.com/szlcsc/TTP223-BA6_C80757.pdf) acts as a touch sensor | It occupies less area and could light up even when it is not worn and just picked up. |
| Darlington Transistor | A 2N5306 Darlington transistor can act as a touch sensor. | 
