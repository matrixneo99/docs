**AWTRIX **

**        Dokumentation (Beta)**

**          von Stephan Mühl**

**Links:**Firmware**: ****[https://github.com/Blueforcer/AWTRI**X](https://github.com/Blueforcer/AWTRIX)****3D-Files**: ****[https://www.thingiverse.com/thing:2791276**](https://www.thingiverse.com/thing:2791276)Facebook**: ****[https://www.facebook.com/groups/126493104851075**/](https://www.facebook.com/groups/126493104851075/)****Kaffeespenden**: ****[http://bit.ly/2HVV21**N](http://bit.ly/2HVV21N)

**Inhaltsverzeichnis**

[[TOC]]

# **Elektronik**

Die Elektronik kann entweder auf Lochrasterplatine gelötet oder "fliegend" verdrahtet werden. (Platine wird in Zukunft eventuell noch für kleines Geld zu erwerben sein)

An der Matrix direkt zu löten kann fatale Folgen mit sich bringen, da das flexible PCB und vor allem die LEDs extrem Hitzeempfindlich sind. Lasst daher das Kabel am Eingang (DI,5V,GND) und schneidet nur den stecker ab. Sollte eure Matrix einen Ausgang haben (DO) so könnt ihr diesen auch getrost komplett entfernen.Bevor Ihr die Buchse für die Spannungsversorgung fest verlötet, verschraubt Sie erst mit 2 angelöteten Adern am Gehäuse. Wie Ihr alles miteinander verlötet könnt ihr diesem Schema entnehmen:

![image alt text](image_0.jpg)

# **Gehäuse**

## **Druck**

Das Gehäuse kann mit einem 3D-Drucker erstellt werden. Die notwendigen Files können von Thingyverse heruntergeladen werden.[https://www.thingiverse.com/thing:2791276](https://www.thingiverse.com/thing:2791276)

Die 3D Objekte sind bereits so ausgerichtet wie sie auch gedruckt werden sollten, um so wenig Support-Material wie möglich zu benötigen. Bitte das **LED-Grid in Schwarz **drucken, ansonsten sind die "Pixel" nicht klar voneinander getrennt, da sie durch das Material scheinen.**Empfohlene Druckeinstellungen:**

* 0,2 mm Schichtauflösung

* 20% Infill

* Support vom Druckbett aus

* 45-55 mm/s

## **Montage**

Zuerst werden die 2 Teile des LED-grids an der Innenseite miteinander verklebt. Die Flache Seite mit einem Klebestift einschmieren und festes Zeichenpapier (ca 190 g/m²) aufkleben und zuschneiden. Dasselbe mit den 2 teilen des Front-Rahmens.Die hinteren Gehäuseteile ineinander stecken und prüfen das diese perfekt passen. Sie sollten nur mit leichtem Druck zusammengesteckt werden können. Bei zu viel Spannung kann sich das Gehäuse später durch die Hitze der LEDs verbiegen. Schleifpapier ist ein gutes Hilfsmittel um alles passend zu machen, falls der Drucker nicht perfekt eingestellt ist. Wenn alles passt können die Gehäuseteile ebenfalls miteinander verklebt werden.

Danach kann die Elektronik eingesetzt werden (In Zukunft wird es evtl eine Platine geben, um das etwas sauberer zu gestalten).

Das LED-Grid auf die Vorderseite legen und die Matrix kopfüber einlegen, diese sollte perfekt in die Nut passen. Nun kann das Gehäuse auf das Grid gedrückt werden. Das ganze einmal umdrehen und den Rahmen aufstecken.

# **Software**

## **Entwicklungsumgebung**

Zum bearbeiten und Upload der Firmware wird Platform.IO verwendet.

Hierbei ist die zugrunde liegende IDE (Atom, Visual Studio Code)  egal.

Diese Anleitung basiert jedoch auf Visual Studio Code und muss ggf. adaptiert werden.

Die Installation der IDE wird in folgendem Link beschrieben:[https://platformio.org/platformio-ide](https://platformio.org/platformio-ide)

## **Download und öffnen der Firmware**

Die Firmware kann bei github als ZIP heruntergeladen werden[https://github.com/Blueforcer/AWTRIX](https://github.com/Blueforcer/AWTRIX)![image alt text](image_1.png)

Die ZIP Datei mit einem geeigneten Entpacker entpacken und den Ordner in Visual Studio Code öffnen.

## **AWTRIX Konfiguration**

Die Konfiguration besteht aus 2 Teilen. 

Zum einen die Einstellungen für die Anzeige und zum anderen die Konfiguration der API Schlüssel der einzelnen Apps. Beide Dateien befinden sich im root verzeichnis.und müssen vor dem Upload umbenannt werden und in den ordner "**data**" kopiert werden.  

### **Settings**

Die Einstellungen werden in der "**settings.example.json**" angepasst. In der Datei selbst finden sich auch die Erklärungen der einzelnen Einstellungen. *Bevor die Datei hochgeladen wird, ist es wichtig, die Datei in “***_settings.json_***” umzubenennen und in den ordner “***_data_***” zu kopieren.*

### **Config**

Die Konfiguration wird in der "**config.example.json**" angepasst.  *Bevor die Datei hochgeladen wird, ist es wichtig, die Datei in ***_“config.json” _***umzubenennen und in den ordner “***_data_***” zu kopieren.*

**Wunderground API (wird zur Wetteranzeige benötigt):**Alle nötigen Daten können mit einem kostenlosen Account auf [https://www.wunderground.com/weather/api/?MR=1 ](https://www.wunderground.com/weather/api/?MR=1)geholt werden.

Der ZMW Code kann über [http://autocomplete.wunderground.com/aq?query=Frankfurt](http://autocomplete.wunderground.com/aq?query=Frankfurt) entnommen werden. (Name des Ortes/Stadt anpassen)

**Youtube API (wird für die Youtube-App benötigt)**

Diese Anleitung befolgen (Letzer Schritt ist nicht nötig)

[https://www.vimp.com/de/web/faq-medien/items/wie-erstelle-ich-einen-youtube-api-key.html](https://www.vimp.com/de/web/faq-medien/items/wie-erstelle-ich-einen-youtube-api-key.html)

**Facebook API (Wird für die Facebook-App) benötigt**

Die URL setzt sich wie folgt zusammen:*/AAA?access_token=BBB|CCC&fields=fan_count*

und besteht aus 

*AAA = Facebook Page ID oder Name,*

*BBB = App ID*

*CCC = App Secret***Für diese Daten muss eine Facebook App erstellt werden: [https://developers.facebook.com/](https://developers.facebook.com/)

Den Fingerprint bekommt man so:

[https://github.com/gbrault/esp8266-Arduino/blob/master/doc/esp8266wifi/client-secure-examples.md#how-to-verify-servers-identity](https://github.com/gbrault/esp8266-Arduino/blob/master/doc/esp8266wifi/client-secure-examples.md#how-to-verify-servers-identity)

## **Upload auf ESP8266**

Nachdem alle Einstellungen erledigt sind kann die Firmware per USB hochgeladen werden:In VSC geschieht dies in der blauen Zeile unten am Fensterrand:![image alt text](image_2.png)

Danach müssen die settings.json sowie die config.json in den Flashspeicher (SPIFFS) geladen werden. Dies geschieht über den Terminal Befehl: (das Terminal lässt sich über das ganz rechte Symbol starten). Überprüft, dass sich beide Dateien mit dem richtigen namen im Ordner "data" befinden

**platformio run -t uploadfs **

## **Erster Start**

Nachdem die Firmware erfolgreich auf den ESP8266 geladen wurde, startet AWTRIX einen WLAN Accesspoint. "AP" wird auf Awtrix angezeigt. Sucht mit eurem WLAN fähigen Gerät nach dem offenen Netzwerk “AWTRIX” und verbindet euch. Danach öffnet einen Webbrowser und gebt in die Adresszeile

**192.168.4.1** ein. Dort habt ihr die Möglichkeit, AWTRIX mit eurem eigenen WLAN zu verbinden. Eine Internetverbindung ist für AWTRIX zwingend notwendig. 

## **Updatemöglichkeiten**

Weitere Updatemöglichkeit bestehen nach dem erstmaligen flashen per USB:**Update per WLAN:**

AWTRIX unterstützt Over-the-Air updates. Terminal:**platformio run -t upload --upload-port 192.168.178.96**

Hierbei die IP Adresse anpassen. Diese Variante funktioniert auch beim flashen des SPIFFS **platformio run -t uploadfs --upload-port 192.168.178.96**

**Update per Web:**

AWTRIX unterstützt das Hochladen der Firmware über den Webbrowser.

Die Webseite **http://IP-VON-AWTRIX/update** in einem Browser eingeben.

Benutzername "awtrix" Passwort “admin” eingeben und die “firmware.bin” auswählen.

Hiermit kann **nicht** die Konfiguration geupdatet werden.

**Automatische Updates:**

In den Einstellungen muss lediglich das Automatische update aktiviert werden.

Nach jedem Neustart von AWTRIX wird auf eine neue Firmware geprüft und ggf automatisch installiert.

## **Fernsteuern mit der BLYNK App**

AWTRIX kann über die BLYNK App ferngesteuert werden. Alle Einstellungen werden nach dem Neustart von AWTRIX beibehalten.

Die App ist für iOS und Android verfügbar. Mit folgendem Link oder  QR-Code kann die fertige BLYNK konfiguration von mir geladen werden. [http://tinyurl.com/y9fo3wfl](http://tinyurl.com/y9fo3wfl)Danach kann sie beliebig verändert werden.

(Achtung: Da viele Steuerelemente benötigt werden ist es nötig Energy per In-App-Kauf zu holen. Ich empfehle mindestens 5000 zu kaufen um nachfolgende Updates abdecken zu können).In der App findet man auch den API-Key welcher in der config.json eingetragen werden muss.Bei Updates wird die App leider nicht automatisch aktualisiert. Das neue BLYNK Layout wird in der Facebookgruppe und hier aktuell gehalten.

## **Ändern der App-Reihenfolge**

Momentan ist es nur über den Quellcode möglich die Reihenfolge in der die Apps angezeigt werden zu ändern. Die geht allerdings einfach. Öffnet die main.cpp und ändert einfach die Reihenfolge folgender Zeilen. Es ist allerdings zu beachten das ein Firmware update eure Reihenfolge wieder zerstören wird. Es wird an einer einfachen Lösung gearbeitet.

![image alt text](image_3.png)

## **Erstellung eigener AWTRIX Apps**

folgt...

 

