# This section is still under development. Ignore it!
___
  
![image alt text](assets/code.png)

# Programming language  
AWTRIX and its Apps are written in B4X Language. 
B4X uses a Proprietary dialect of Visual Basic (hereinafter called "B4X").

# IDE (development environment)
B4J – Modern “VB6 like” development tool for cross platform desktop, server and IoT solutions B4J is a 100% free development tool for
desktop, server and IoT solutions. With B4J you can easily create desktop applications (UI), console programs (non-UI) and server solutions.
The compiled apps can run on Windows, Mac, Linux and ARM boards (such as Raspberry Pi). The compiled Apps are native Java applications.  
  
[Download B4J](https://www.b4x.com/b4j.html)


# Apps definition
AWTRIX Apps are Java libraries that can be loaded at runtime.
Defined functions called by AWTRIX transfer the information about the screen layout.

# Procedure 
The functions are divided into 4 main parts:  
  
**Initialization**  
AWTRIX initializes the app and checks if all necessary settings parameters are set. If so, the app will be included in AWTRIX's internal apploop.  

**Start**  
At every start AWTRIX asks for the desired tickrate (in ms) in which the drawing routine should be called.It also return the set app duration to know how long this app will be active.

**Rendering**  
AWTRIX called the function each set Tick.
AWTRIX expects, with each tick, a list of all drawingcommands that represent a frame.
After receiving this list, AWTRIX draws all commands step by step and then displays the finished rendered frame.

**Update**
While updating, AWTRIX asks the APP how many Downloads are needed (ususal one). Then (for each singe download) it requests the URL for the desired data, download it, and return the response as String and InputStream for further porcessing inside the App.
AWTRIX has an global configurable Updateinterval after wich every App will be updated. The user can also force each app to update after a specific timespan.