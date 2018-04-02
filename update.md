## **Update**

Further update options are available after the first flashing via USB:

**Update via WiFi:**

AWTRIX supports over-the-air updates. Terminal:
platform run -t upload --upload port 192.168.178.96**

Adjust the IP address. 
This variant also works when flashing the SPIFFS 
platform run -t uploadfs --upload port 192.168.178.96**

**Update via Web:***

AWTRIX supports firmware upload via web browser.

Enter the web page **http://IP-FROM-AWTRIX/update** in a browser.

Enter user name "awtrix", password "admin" and select the "firmware.bin".


**Automatic updates:**

In the settings only the automatic update must be activated.

After each restart of AWTRIX a new firmware is checked and installed automatically if necessary.