## API Definition

You can control Awtrix via UDP or MQTT. 

**UDP**
With UPD Awtrix listens to the port 52829. 
Each API command is exactly one UDP packet containing one line.   
If you send a known command, Awtrix send "ACK" as a response back to the remoteIP.  
**MQTT**
With MQTT Awtrix listens to the Topic "awtrix/com".
If you send a known command, Awtrix send "ACK" to Topic "awtrix/com/response".  
  
Some commands consist of the command itself and a payload which is passed, separated by a percentage symbol (%).      

**Commands**

| COMMAND | PAYLOAD | EXAMPLE | DESCRIPTION | UDP | MQTT 
| ------ | ------ | ------ | ------ |
| bri | 1-255 | bri%50 | Sets the Matrix Brightness to the given payload | X | X 
| color | HEX | color%#4286f4 | Sets the textcolor to the given payload | X | X 
| mood | 0-3 | mood%2 | Change the emotion of the virtual pet | X | X 
| text | STRING | text%Hello World | Scroll the given text | X | X 
| save | - | save | Save all Settings to the flash memory | X | X 
| reset | - | reset | reset Awtrix | X | X 
| next | - | next | Switch to next Application | X | X 
| gamemode | 0-1 | gamemode%1 | Activate gamingmode | X | X 
| game | 0-1 | game%1 | Change the Game (0=Snake/1=Pong) | X | X 
| pongmove | 0-1000 | pongmove%500 | Move the paddle from left to right | X | - 
| snakemove | 0-3 | snakemove%1 | Change the Snake direction (0=TOP/1=RIGHT/2=BOTTOM/3=LEFT) | X | - 
| settings | get | settings%get | Send back all Settings as one JSON | X | - 
| settings | JSON | settings&{"BIG_TIME": "1"} | Save all Settings from the given JSON to Flash. You can send any number of settings in a JSON  | X | - 
