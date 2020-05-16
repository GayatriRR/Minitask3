## TASK 1: SMART RING 

### Constraints:
It being a ring brings a big constraint in the form of **size**. Moreover, as it is going to be worn, the **heating effect** should be less. **Current** through the circuit should be maintained low to make it as safe as possible. The components also must have a **sleep/low power mode** to minimise the power lost while it is not being used.

### Ideation:
As the presence of an external switch is the problem with the system in the first place, we need an internal switch in the circuit which will let the LED glow when the ring is worn. To ponder on the possible solutions, we need to analyse what haappens when the ring is worn:
* The finger touches the inner part of the ring.
* The inner area of the ring is cut off from light.
* A pressure is applied on the inner surface of the ring.


| Idea | Implementation | Comments |
|-------------------|--------------------|--------------------|
| External trigger based switch | Some external component, similar to a mini-button to which can switch on the circuit when pressed. | Simple. But can cause discomfort. |
| Capacitive Touch sensor | A [TTP223](https://datasheet.lcsc.com/szlcsc/TTP223-BA6_C80757.pdf) acts as a touch sensor | It occupies less area. But it could light up even when it is not worn and just picked up. |
| Darlington Transistor | A [BSP52](https://www.mouser.in/datasheet/2/308/BSP52T1-D-1803012.pdf) Darlington transistor can act as a touch sensor. The priciple is such that the small current that our body produces must get amplified to such a factor that the LED is able to light up. This ensures safety due to small current flowing through the body (order of micro amperes). | We need the finger to complete the circuit and this means some level of challenge in the design of the circuit. On the other hand, it is a simple, safe and compact circuit to implement. |
| LDR based circuit | When the ring is worn in hand, the inner surface becomes dark, which is detected by the LDR making the LED light up. | The components used are small and compatible. But the circuit could light up when it is kept in a dark enclosure. Thus this might need an extra switch to switch off the circuit when the ring is not likely to be used. |

* The best option is to use a **capacitive sensor** which is a copatible solution as it is **not costly**, has a **low power mode** and has a **compact structure**. 
* The supply is chosen to be the button cell of supply 3V which can be used for operating the touch sensor too. 
* A microprocessor is not necessary in the simplest mode of operation, but if necessary, an ATtiny45 could be used which can operate at the same supply.
