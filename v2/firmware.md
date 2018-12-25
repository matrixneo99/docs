## **IDE**

Platform.IO is used to edit and upload the firmware.

The underlying IDE (Atom, Visual Studio Code) does not matter.

However, this manual is based on Visual Studio code and may need to be adapted.

The installation of the IDE is described in the following link:
[https://platformio.org/platformio-ide](https://platformio.org/platformio-ide)

## **Flashing**

The firmware can be downloaded here:
[AWTRIX Controller](#)


Unzip the ZIP file with a suitable unpacker and open the folder in Visual Studio code. Then simply flash the firmware. In VSC, this is done in the blue line at the bottom of the window:  

![image alt text](assets/image_2.png)

## **Setup**
After successfully uploading the firmware, the AWTRIXController starts a WiFi hotspot, connect to your mobile phone with this open access point and enter the address for the Wifi configuration into a webbrowser:   
http://192.168.4.1/

In the first menu item you can configure your WiFi.  
!> **You also have to enter the IP address of the AWTRIX host in the last input field.**


## **Troubleshooting**
If the access point does not appear after successful flashing, the flash memory of the ESP must be reset.
To do this download the Flash Download Tools (ESP8266 & ESP32)
 from [here](https://www.espressif.com/en/support/download/other-tools), start it and click on Erase, then flash the ESP once again.

If your Matrix shows weird Pixel and you cant read it, you have to flash the Firmware again but set the Matrixmode 2:  
just uncomment following line in awtrixcontroller.cpp   
```#define MATRIX_MODEV2```