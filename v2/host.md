AWTRIX 2.0 can run on any platform (Windows, MacOS, Linux), the only requirement is the support of Java8. It is a non-GUI application so you doesnt need an desktop enviroment.   
This Tutorial describes the installation on a Linux machine (in my case a Raspberry ZeroW with Rasbian Lite)

First check if Java is installed  
```java -version```  
  
Otherwise install the latest Java8:  
```sudo apt-get install oracle-java8-jdk```  

Set your timezone: e.g  
``` sudo timedatectl set-timezone Europe/Berlin```  
   
## **Quickstart**
This short example shows how to start the Java application.
Move to the next point for installing on a Linux machine such RaspberryPi

Download the current java  file
[AWTRIX Java application](http://awtrix.blueforcer.de/awtrix.jar)

 and start it via command line or terminal
 ``` sudo java -jar awtrix.jar ```    

!> **sudo** is not always needed. It depends on the folder in wich you want to start the Application. Awtrix need to create new folders and files, so in few cases Awtrix has no write permissions.

Shortly after the start the web interface can be called via http://awtrix_ip:7000.


## **Installing on a Linux machine with Autostart**
```sudo mkdir /usr/local/awtrix```  
```cd /usr/local/awtrix```    
```sudo wget http://awtrix.blueforcer.de/awtrix.jar```



### **Autostart**


Create a file under  **/etc/systemd/system/** with nano or vi. eg.  
```sudo nano /etc/systemd/system/awtrix.service```  
  
Paste the code below in this new file:
```
[Unit]
Description = AWTRIX Service
After network.target = awtrix.service

[Service]
Type = forking
WorkingDirectory =/usr/local/awtrix
ExecStart = /usr/local/bin/awtrix.sh start
ExecStop = /usr/local/bin/awtrix.sh stop
ExecReload = /usr/local/bin/awtrix.sh reload

[Install]
WantedBy=multi-user.target
```


Create a new file under ***/usr/local/bin/*** eg.   
```sudo nano /usr/local/bin/awtrix.sh```  
  
And paste this code
```
#!/bin/sh
SERVICE_NAME=awtrix
PATH_TO_JAR=/usr/local/awtrix/awtrix.jar
PID_PATH_NAME=/tmp/awtrix-pid
case $1 in
    start)
        echo "Starting $SERVICE_NAME ..."
        if [ ! -f $PID_PATH_NAME ]; then
            sudo nohup java -jar $PATH_TO_JAR /tmp 2>> /dev/null >> /dev/null &
                        echo $! > $PID_PATH_NAME
            echo "$SERVICE_NAME started ..."
        else
            echo "$SERVICE_NAME is already running ..."
        fi
    ;;
    stop)
        if [ -f $PID_PATH_NAME ]; then
            PID=$(cat $PID_PATH_NAME);
            echo "$SERVICE_NAME stoping ..."
            kill $PID;
            echo "$SERVICE_NAME stopped ..."
            rm $PID_PATH_NAME
        else
            echo "$SERVICE_NAME is not running ..."
        fi
    ;;
    restart)
        if [ -f $PID_PATH_NAME ]; then
            PID=$(cat $PID_PATH_NAME);
            echo "$SERVICE_NAME stopping ...";
            kill $PID;
            echo "$SERVICE_NAME stopped ...";
            rm $PID_PATH_NAME
            echo "$SERVICE_NAME starting ..."
            sudo nohup java -jar $PATH_TO_JAR /tmp 2>> /dev/null >> /dev/null &
                        echo $! > $PID_PATH_NAME
            echo "$SERVICE_NAME started ..."
        else
            echo "$SERVICE_NAME is not running ..."
        fi
    ;;
esac
```

save the file and give execution permisions

``` sudo chmod +x /usr/local/bin/awtrix.sh``` 


Test that it runs with:  
```sudo /usr/local/bin/./awtrix.sh start```     
Test that it stops with:   
```sudo /usr/local/bin/./awtrix.sh stop```     
Test that it restarts with:  
```sudo /usr/local/bin/./awtrix.sh restart```     

If everything is working, enable the service with the command

```sudo systemctl enable awtrix```  




To run awtrix  
```sudo systemctl start awtrix.service ```   
To stop awtrix   
```sudo systemctl stop awtrix.service```   
To restart awtrix   
```sudo systemctl restart awtrix.service``` 



## **Docker**
**(Only for x64 platforms!)**  

https://hub.docker.com/r/o0shojo0o/awtrix

