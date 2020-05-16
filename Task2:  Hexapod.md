## CONTROL SYSTEMS FOR REINFORCED LEARNING FOR A HEXAPOD

The Hexapod has 6 legs which has 3 degrees of freedom. We need to take information of the movement of the of each leg and reflect the exact same on the computer using reinforced learning.

### IMU Sensor
* For this, there are servo motors which help in the movement of the hexapod. The movement of the hexapod is sensed by IMU sensors, 3 on each leg. A total of 19 IMU sensors must to be send information to the microcontroller. 
* We use [MPU6050](https://components101.com/sensors/mpu6050-module) as the IMU sensor.
* The MPU6030 is interfaced with the microcontroller through the I2C protocol. But the problem with the set-up is that all MPU6030 have the same address of 0x68. 
* For this purpose, the MPU6030 has a AD0 pin which allows the address to be changed when there are more than one MPU6030 used in a circuit. When AD1 is made high, the address of the MPU6030 becomes 0x69.
* Thus all MCU6030 pins have their AD0 pin at default HIGH. When a particular MCU6030 wants to communicate, its AD0 pin becomes LOW. Thus the microcontroller receives information from the device which has an address 0x68. This way, only one IMU sensor has the address 0x68 at a time.

![pi](https://components101.com/sites/default/files/component_pin/MPU6050-Pinout.png)

### I2C Interfacing


