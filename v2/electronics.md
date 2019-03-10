# **Electronic**

The electronics can either be soldered to a breadboard or wired "overhung". (PCB may still be available for a small fee in the future)

Soldering directly to the matrix can have fatal consequences, as the flexible PCB and especially the LEDs are extremely heat-sensitive. Leave the cable at the input (DI,5V,GND) and cut off only the plug. If your matrix has an output (DO), you can remove it completely.
Before soldering the socket for the power supply, screw it to the housing with 2 soldered wires. How you solder everything together can be seen in this scheme:

![image alt text](assets/image_0.jpg)

## Gesture control
You can control AWTRIX with Hand gestures (Only switching between Apps for now) with a APDS-9960 Gesture Sensor
Please keep in mind that the Housing is not prepared for mounting this sensor. You will have to do it by your own.
  
!> IMPORTANT: The APDS-9960 can only accept 3.3V!

| Wemos | APDS-9960 | Function |
| --- | --- | --- |
|3.3V|VCC|Power|
|GND|GND|Ground|
|D3|SDA|I2C Data|
|D1|SCL|I2C Clock|
|D6|INT|Interrupt|