## **Webinterface**

In order to make the operation as simple as possible for everyone, the complete operation takes place via a web interface.
The standard port is 7000.

Here you can manage all your settings, manage your apps and download new one.

![image alt text](assets/web.png)

## **Systemsettings**
Here you will find all relevant settings concerning the operation of AWTRIX.
- **verboseLog**
  - logging mode that records more information than the usual logging mode. 
- **switchAnimation**
  - Whether the transition animation between the apps should be displayed
- **colorSwitch**
  - Another transition animation 
- **uppercaseLetters**
  - Converts  all letters to capital letters
- **textColor**
  - The global texcolor (Red,Green, Blue). All values can be from 0-255 and must be separated by a comma.
- **brightness**
  - The brightness of the matrix (0-255)
- **appDuration**
  - Time in seconds to change to the next app
- **updateInterval**
  - Global interval in which all apps are updated. Exceptions are the apps that were manually overwritten (see MyApps).
- **scrollSpeed**
  - The speed at which the text is scrolled in milliseconds. (The lower the faster, default: 65)
- **autoBrightness**
  - Activates the automatic brightness control. (Only with LDR connected)
- **cloudActive**
  - Enables the cloudconnection
- **webServerPort**
  - Port the Websever listens to
- **MQTTclient**
  - Connects AWTRIX to an existing MQTT Broker

## **MyApps**
The administration of all your apps takes place here.  
Here you can disable, configure or delete your apps  
![image alt text](assets/insta.png)

Every App has its own updateInterval. If it is set to 0, it means that this app together with the other apps will be updated after a global period. (Systemsettings->updateInterval).   
This setting is sufficient for most apps not to exhaust the API quota.  
However, if desired, the interval at which the app fetches new data can be forced. Just enter a timespan in seconds (minimum 10s). 

## **Appstore**
AWTRIX has its own appstore.
Here all tested apps are provided and can be downloaded or updated.
After a download you find this app in MyApps.
