## **Webinterface**

In order to make the operation as simple as possible for everyone, the complete operation takes place via a web interface.
The standard port is 7000.

Here you can manage all your settings, manage your apps and download new one.

![image alt text](assets/appstore.png)

## **Systemsettings**
Here you will find all relevant settings concerning the operation of AWTRIX.

#### General Settings
- **BootAnimation**
  - shows an animation after boot. 
- **SwitchAnimation**
  - Whether the transition animation between the apps should be displayed.
- **ColorSwitch**
  - Another transition animation. 
- **UppercaseLetters**
  - Converts  all letters to capital letters.      
- **VerboseLog**
  - logging mode that records more information than the usual logging mode. 
- **TextColor**
  - The global texcolor (Red, Green, Blue). All values can be from 0-255 and must be separated by a comma.
- **Brightness**
  - The brightness of the matrix (0-255).
- **AppDuration**
  - Time in seconds to change to the next app.
- **UpdateInterval**
  - Global interval in which all apps are updated. Exceptions are the apps that were manually overwritten (see MyApps).
- **ScrollSpeed**
  - The speed at which the text is scrolled in milliseconds. (The lower the faster, default: 65).  
  
### Automatic Brightness   
- **AutoBrightness**
  - Activates the automatic brightness control. (Only with LDR connected).
    
### Connections   
 After changing you need to restart the server 
- **webServerPort**
  - Port the Webserver listens to.

### USB    
 After changing you need to restart the server
- **USBMatrix**
  - Enable to connect the Matrix via USB (Serialconnection).
    to the server. You need to activate USB also in the AWTRIXcontroller (min. v0.7).
- **USBPort**
  - If USBPort "auto" (for autodetection) doesnt work, you need to insert the Port manually (e.g. "COM5" or "/dev/ttyUSB0")
  
### MQTT 
 After changing you need to restart the server
- **MQTTclient**
  - Connects AWTRIX to an existing MQTT Broker.

## Premium

!> This features are only available with a premium subscription. This subscription will be available later. 
Until then, these functions are absolutely free and fully usable.

 After changing you need to restart the server

- **CloudActive**
  - Enables the Cloud connection.

- **Telegram**
  - enables the bot to control AWTRIX with the telegram messenger.
    To get your BotToken you need to create your bot with BotFather in Telegram.  

- **FritzCaller**
  - Enables the Fritz!Box Call monitor, and displays incoming calls.    
!> The CallMonitor function on the Fritz!Box must be activated (e.g. by entering #96*5* on a telephone connected to the Fritz!Box).
You can also add your Fritz!Box phone book, by export it and [convert the xml to json](http://www.utilities-online.info/xmltojson/). Save it as "fritzbox.json" in the config folder. AWTRIX will show the caller names after restart.

- **FritzBoxIP**
  - IP adress of your Fritzbox (needed for FritzCaller).  


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

<img src="v2/assets/Sunrise.png" height="36" width="36"> **Sunrise**  
Shows sunset and sunrise times for a given location.  
https://www.sunrise-sunset.org 

<img src="v2/assets/GameOfLife.png" height="36" width="36"> **GameOfLife**  
Conway's Game of Life  
Internal App

<img src="v2/assets/LookingEyes.png" height="36" width="36"> **LookingEyes**  
Just some looking eyes :)   
Internal App

<img src="v2/assets/Matrix.png" height="36" width="36"> **Matrix**  
Shows the popular Matrix animation.  
Internal App

<img src="v2/assets/PeopleInSpace.png" height="36" width="36"> **PeopleInSpace**  
Shows how many people are in space right now.     
https://www.howmanypeopleareinspacerightnow.com/ 

<img src="v2/assets/mixer.png" height="36" width="36"> **mixer**  
Shows your mixer subscriber count or your live viewers while youre streaming.     
https://mixer.com/  

<img src="v2/assets/OpenWeather.png" height="36" width="36"> **OpenWeather**  
Shows the current temperature of your location.    
https://openweathermap.org/  

<img src="v2/assets/pr0gramm.png" height="36" width="36"> **pr0gramm**  
Show the lenght of your Benis.     
https://pr0gramm.com  

<img src="v2/assets/MinecraftServer.png" height="36" width="36"> **MinecraftServer**  
Shows the player count of a Minecraft Server.  
Only appears if the server is online.  
https://www.minecraft.net  

<img src="v2/assets/MyStrom.png" height="36" width="36"> **mystrom**  
Shows the state and power consumption of your MyStrom SmartPlug.  
https://mystrom.com/  

<img src="v2/assets/QuitSmoking.png" height="36" width="36"> **QuitSmoking**  
Shows the days how long you don't smoke anymore.  
Internal App  

<img src="v2/assets/TronaldDump.png" height="36" width="36"> **TronalDump**  
Shows the dumbest things Donald Trump has ever said.  
https://tronalddump.io  

<img src="v2/assets/Countdown.png" height="36" width="36"> **Countdown**  
Shows the remaining days from now to a target date.  
Internal App  

<img src="v2/assets/Crypto.png" height="36" width="36"> **Crypto**  
Shows prices for any cryptocurrency. Set your desired Coin and your currency.   
Internal App  

<img src="v2/assets/facebook.png" height="36" width="36"> **facebook**  
Shows your Facebooksite likes count.   
www.facebook.com  

<img src="v2/assets/fortnite.png" height="36" width="36"> **fortnite**  
Shows your Kills, Wins, Wins% and K/D.   
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
