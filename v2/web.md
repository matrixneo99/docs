## **Webinterface**

In order to make the operation as simple as possible for everyone, the complete operation takes place via a web interface.
The standard port is 7000.

Here you can manage all your settings, manage your apps and download new one.

![image alt text](assets/web.png)

## **Systemsettings**
Here you will find all relevant settings concerning the operation of Awtrix. Like e.g. brightness, text color or connection settings

## **MyApps**
The administration of all your apps takes place here.
Here you can configure or delete your apps  
![image alt text](assets/insta.png)

Every App has its own updateInterval. If it is set to 0, it means that this app together with the other apps will be updated after a global period. (Systemsettings->updateInterval).   
This setting is sufficient for most apps not to exhaust the API quota.  
However, if desired, the interval at which the app fetches new data can be forced. Just enter a timespan in seconds (minimum 10s). 

## **Appstore**
Awtrix has its own appstore.
Here all tested apps are provided and can be downloaded or updated.
After a download you find this app in MyApps. New apps are only displayed if they have been set up.
