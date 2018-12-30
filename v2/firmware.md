## **IDE**

Platform.IO is used to edit and upload the firmware.

The underlying IDE (Atom, Visual Studio Code) does not matter.

However, this manual is based on Visual Studio code and may need to be adapted.

The installation of the IDE is described in the following link:
[https://platformio.org/platformio-ide](https://platformio.org/platformio-ide)

## **Flashing**

The firmware can be downloaded here:
[AWTRIX Controller](http://awtrix.blueforcer.de/awtrixcontroller.zip)


Unzip the ZIP file with a suitable unpacker and open the folder in Visual Studio code. Then simply flash the firmware. In VSC, this is done in the blue line at the bottom of the window:  

![image alt text](assets/image_2.png)

## **Setup**

After successfully uploading the firmware(e.g. Blue LED is permanently illuminated), the AWTRIXController starts an own WiFi hotspot (named as AWTRIXController), connect to your mobile phone with this open access point(no pw required hotspot AWTRIXController) and enter the address for the WiFi configuration into a web browser.

- Connect to WiFi hotspot "AWTRIXController".
- Visit http://192.168.4.1/ to enter the configuration menu.
- Enter the credentials of your own WiFi network in the configuration.  
- Enter the IP address of the AWTRIX host in the last input field.


## **Troubleshooting**

If the access point does not appear after successful flashing or something went wrong, the flash memory of the ESP must be reset. To do this download the Flash Download Tools (ESP8266 & ESP32) from [here](https://www.espressif.com/en/support/download/other-tools), click on Erase, then flash the ESP once again.

- Download the [tool](https://www.espressif.com/en/support/download/other-tools).
- Unzip it.
- Start the flash tool exe.
  - Select your uC accordingly from the available configuration menu.
  - Navigate to SPIDownload.
  - Configure the COM-Port and Baud Rate.
  - Click on Erase Button to delete the flash finally.

If your Matrix shows weird Pixel and you cant read it, you have to change code and flash the Firmware again, by setting the Matrixmode 2:
- just uncomment following line in awtrixcontroller.cpp   
```#define MATRIX_MODEV2```
- repeat steps from chapter **Flashing**