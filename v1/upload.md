## **Upload to ESP8266**

After all settings are done, the firmware can be uploaded via USB:
In VSC, this is done in the blue line at the bottom of the window:  

![image alt text](assets/image_2.png)

Then the settings.json and the config.json must be loaded into the flash memory (SPIFFS).  Check that both json files with the correct name are in the folder "data" and run

> **platformio run -t uploadfs **

This is done via the Terminal. The Terminal can be started via the rightmost icon.