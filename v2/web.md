## **Webinterface**

In order to make the operation as simple as possible for everyone, the complete operation takes place via a web interface.
The standard port is 7000.

Here you can manage all your settings, manage your apps and download new one.

![image alt text](assets/web.png)

## **Systemsettings**
Here you will find all relevant settings concerning the operation of AWTRIX.

### General Settings     
- **verboseLog**
  - logging mode that records more information than the usual logging mode. 
- **switchAnimation**
  - Whether the transition animation between the apps should be displayed.
- **colorSwitch**
  - Another transition animation. 
- **uppercaseLetters**
  - Converts  all letters to capital letters.
- **textColor**
  - The global texcolor (Red, Green, Blue). All values can be from 0-255 and must be separated by a comma.
- **brightness**
  - The brightness of the matrix (0-255).
- **appDuration**
  - Time in seconds to change to the next app.
- **updateInterval**
  - Global interval in which all apps are updated. Exceptions are the apps that were manually overwritten (see MyApps).
- **scrollSpeed**
  - The speed at which the text is scrolled in milliseconds. (The lower the faster, default: 65).  
  
### Automatic Brightness   
- **autoBrightness**
  - Activates the automatic brightness control. (Only with LDR connected).
    
### Connections    
- **cloudActive**
  - Enables the cloud connection.
- **FritzCaller**
  - Enables the Fritz!Box Call monitor, and displays incoming calls.
    
?> The CallMonitor function on the Fritz!Box must be activated (e.g. by entering #96*5* on a telephone connected to the Fritz!Box).
You can also add your Fritz!Box phone book, by export it and [convert the xml to json](http://www.utilities-online.info/xmltojson/). Save it as "fritzbox.json" in the config folder. AWTRIX will show the caller names after restart.

- **webServerPort**
  - Port the Webserver listens to.
- **FritzBoxIP**
  - IP adress of your Fritzbox (needed for FritzCaller).  
   
### MQTT 
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
 
<img src="v2/assets/crypto.png" height="36" width="36"> **crypto**  
Shows prices for any cryptocurrency. Set your desired Coin and your currency.   

<img src="v2/assets/facebook.png" height="36" width="36"> **facebook**  
Shows your Facebooksite likes count.   
www.facebook.com  

<img src="v2/assets/fortnite.png" height="36" width="36"> **fortnite**  
Shows your Kills, Wins, Wins% and K/D   
https://www.epicgames.com/fortnite/de/home  

<img src="v2/assets/gas.png" height="36" width="36"> **gas**  
Zeigt dir die Spritpreise in deiner Naehe an.(Tankerkoenig API)  
www.tankerkoenig.de  

<img src="v2/assets/instagram.png" height="36" width="36"> **instagram**  
Shows your Instagram follower count.   
www.instagram.com  

<img src="v2/assets/matomo.png" height="36" width="36"> **matomo**  
Shows you the visitors of the transferred Matomo instance who were online during the given time period.  
http://matomo.org  

<img src="v2/assets/moon.png" height="36" width="36"> **moon**  
Get Today's Moon Phase with current viewing information.  
Internal App  

<img src="v2/assets/news.png" height="36" width="36"> **news**  
This app provides live top and breaking headlines for your country.  
http://newsapi.org  

<img src="v2/assets/octoprint.png" height="36" width="36"> **octoprint**  
Shows the percentage of progress and remaining time of OctoPrint printing.  
http://octoprint.org  

<img src="v2/assets/overwatch.png" height="36" width="36"> **overwatch**  
Shows your current Skillranking.  
http://playoverwatch.com  

<img src="v2/assets/pinteresr.png" height="36" width="36"> **pinterest**  
Shows your pinterest follower count.  
www.pinterest.com  

<img src="v2/assets/pm.png" height="36" width="36"> **pm**  
Shows the atmospheric particulate matter (PM).  
https://openaq.org/#/map

<img src="v2/assets/speedtest.png" height="36" width="36"> **speedtest**  
Measures the time between the Frames.  
Internal App  

<img src="v2/assets/twitch.png" height="36" width="36"> **twitch**  
Shows your Twitch subscriber count or your live viewers while you are streaming.  
www.twitch.tv  

<img src="v2/assets/twitter.png" height="36" width="36"> **twitter**  
Shows your Twitter Follower count.  
http://twitter.com  

<img src="v2/assets/weather.png" height="36" width="36"> **weather**  
Shows the current temperature of your location.  
www.apixu.com  

<img src="v2/assets/wetterdienst.png" height="36" width="36"> **wetterdienst**    
Displays weather-warnings of Deutscher Wetterdienst.  
Only appears if there is at least one warning.  
https://www.dwd.de/DE/leistungen/opendata/help/warnungen/cap_warncellids_csv.csv/

<img src="v2/assets/youtube.png" height="36" width="36"> **youtube**  
Shows your Youtube subscriber count.  
www.youtube.com  
