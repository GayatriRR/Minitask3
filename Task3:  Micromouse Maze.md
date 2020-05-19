## MICROMOUSE MAZE
### Constraints:
* Dimensions: Should be within 16cm x 16cm x 100cm 
* Within the Techsoc budget
* Sense

### Existing solution:
* Microcontroller: ESP32
* Power: iBall Power Bank 5V
* Chassis: Made from General Purpose Circuit Board
* Wiring: Jumper wires
* Sensors: 2 TOF sensors (VL53L0X): for the sides; 1 Ultrasonic sensor (front)
* Motors with encoders
* Software part: Arduino IDE + Flood fill algorithm + Proportional control for straight line travel

### Suggestions:
**[1.](https://miro.medium.com/max/2000/1*bFJAh4ErlEx7rPRMg96Tpw.png)** We don't exactly need a Bluetooth or Wifi module for the circuit, thus even though a lot of suggestions are in favour of an Arduino, an [STM32](https://www.electronicscomp.com/stm32f103c8t6-minimum-system-board-stm32-arm-module-india) is a better option. The STM32 is compact, has enough memory, enough I/O pins and has faster processing than an Arduino. It can be developed on the Arduino IDE itself.

![as](https://miro.medium.com/max/2000/1*bFJAh4ErlEx7rPRMg96Tpw.png)


**[2.](https://www.youtube.com/watch?v=xO5_3SjEhS4)** Sensors: We use both TOF sensors and ultrasonic sensors in the project.

| Comparison parameter | Distance sensor | TOF sensor |
|---------------------|--------------|-------------|
| Range | 2cm-400cm | 10cm-180cm |
| Working voltage voltage | 5Vdc | 3-5 Vdc |
| Working current | 15mA | 35 mA |
| Dimensions | 45mm x 20mm x 15mm | 20mm x 13mm x 5mm |
| Cost | Lower cost | Higher cost |
| Environment factors | Exposed to environment (affeted by tempertature and humidity) | Sealed to environment |
| Connections | Digital I/O connection | Serial connection and I2C |
| Response | Slow response | Quick response |
| ROF | Wider range of field | Narrow range of field |

From the above, we see that the TOF sensor has a faster response and smaller in size. Moreover, it offers a more accurate measurement than an ultrasonic sensor (this feature is not very necessary feature for a maze solver); but on the downside, the TOF sensor costs more. If two TOF sensors can be afforded, it is better to continue using them in the project. 

3. It would be better to use a circular chassis if it can be afforded. But for a micromouse under the TechSoc budget, the current design is the best.

4. We could continue using the Arduino IDE for the project. 



