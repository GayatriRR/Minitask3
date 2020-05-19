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
1. We don't exactly need a Bluetooth or Wifi module for the circuit, thus even though a lot of suggestions are in favour of an Arduino, an [STM32](https://www.electronicscomp.com/stm32f103c8t6-minimum-system-board-stm32-arm-module-india) is a better option. The STM32 is compact, has enough memory, enough I/O pins and has faster processing than an Arduino. It can be developed on the Arduino IDE itself.

![as](https://miro.medium.com/max/2000/1*bFJAh4ErlEx7rPRMg96Tpw.png)


Distance sensor | TOF sensor
range: 2cm-400cm | 10cm-180cm
5Vdc | 3-5 Vdc
15mA | 35 mA
45*20*15mm | 20*13*5 mm
low cost | higer cost
Exposed to environment | sealed to environment
digital I/O connection | serial connection and I2C 
slow response | quick response
wider range of field | narrow range of field



