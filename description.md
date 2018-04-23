## How it works

AWTRIX includes a variety of apps that can display different functions. All activated apps are looped one after the other. The adjustable time in which an app is displayed is the same for each app. Each function can be activated in the settings.json.


**Sleep Mode**

the sleep mode can be activated by setting a time period via blynk or the Settings.json.
During this period Awtrix only displays the time (strongly darkened). 

**Rainbow mode**

When Rainbow mode is on, the set text color is ignored and each text is displayed in rainbow colors.

**Amazon Alexa**

Awtrix can be turned on and off by Alexa.
you have to activate Alexa in the Settings.json.
After searching for new devices, Awtrix is recognized as "Atrix".


**Here is an explanation of how each officially available app works:**

  
**TimeApp**

Displays the current time and date rotationally. The time is synchronized with a time server (NTP) every 3 minutes. The BIG_TIME setting changes the type of display.

In addition, the current day of the week can be displayed at the bottom of the screen. Here 7 strokes are drawn which stand for all 7 weekdays (Monday-Sunday). The current day of the week is displayed in white, while the remaining days are displayed in gray. AWTRIX supports the automatic summer and winter time changeover.

  

**WeatherApp**

shows the current weather with an icon. Furthermore, the current temperature of the configured location is displayed. The data is downloaded from Openweatermap.

  

**Pet**

Shows 2 eyes that look and blink randomly in all directions. The displayed emotion changes via the setting PET_MOOD.

  

**GOL**  
Represents the game of the mathematician [John Horton Conway](https://de.wikipedia.org/wiki/John_Horton_Conway).  
Rules of the game: [https://de.wikipedia.org/wiki/Conways_game_of_life](https://de.wikipedia.org/wiki/Conways_game_of_life)

  

**FacebookApp**

shows the current likes of a Facebook page.

  

**YoutubeApp**

shows the number of subscribers to a YouTube channel.

  

**TwitterApp**

shows the number of followers of a Twitter profile.

  

**FireApp**

simulates a fire source

  

**DHTApp**

displays the values of a DHT11 or DHT22 sensor. The display changes between temperature and humidity each time the app is restarted.