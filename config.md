## **AWTRIX Configuration**
The configuration consists of 2 parts. 
On the one hand the settings for the display and on the other hand the configuration of the API keys of the individual apps. Both files are located in the root directory.
and must be renamed and copied to the folder "data" before uploading.  

**Settings**
The settings are adjusted in "settings.example.json". The file itself also contains the explanations of the individual settings. Before uploading the file, it is important to rename it to "settings.json" and copy it to the "data" folder.

**Config**
The configuration is adapted in "config.example.json".  Before uploading the file, it is important to rename it to "config.json" and copy it to the "data" folder.


Openweathermap API (required for weather display):
All necessary data can be obtained with a free account at http://openweathermap.org/appid

the OWM Location (City-ID) can be taken from the link after the weather search of the location (e.g. http://openweathermap.org/city/2874230)

Youtube API (required for the Youtube app)
Follow these instructions (last step is not necessary)
https://www.vimp.com/de/web/faq-medien/items/wie-erstelle-ich-einen-youtube-api-key.html


Facebook API (required for the Facebook app)
The URL is composed as follows:
/AAA?access_token=BBB|CCC&fields=fan_count
and consists of 
AAA = Facebook Page ID or Name,
BBB = App ID
CCC = App Secret
A Facebook App must be created for this data: 
https://developers.facebook.com/


That's how you get the fingerprint:
https://github.com/gbrault/esp8266-Arduino/blob/master/doc/esp8266wifi/client-secure-examples.md#how-to-verify-servers-identity
