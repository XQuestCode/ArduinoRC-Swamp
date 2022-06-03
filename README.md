# ArduinoRC-Swamp
Communication between two RC controlled car using 3 HC05 modules
**Instructions on binding HC05 to the slave's HC05**
\na. Connect slave to the the aruino, upload a new sketch. [here](https://pastebin.com/WQsq0igT)
b. Connect Rx pin to Rx of arduino and Tx to Tx of arduino.
c. go to AT mode of HC05 (_hold button for few seconds while powering up, result in slow blinks_)
d. Open serial monitor, set the baud rate to 38400.
e. Type **AT** to check if everything is correct (results an OK reply)
f. Type **AT+ADDR?** (result in something like **+ADDR:0019:10:08FED3** )
g. Now unplug this HC05, and connect the Master HC05.
h. Go to AT mode.
i. Type **AT+ROLE=1**
j Type **AT+BIND = 0019,10,08FED3** (your slave address)
k. Good to go, power them seperately, and they are ready to be binded



#Instructions on making Bluetooth controlled RC car
https://github.com/XQuestCode/Arduino-Bluetooth-RC-car

#Video guide 
https://youtu.be/pGfxNgYMi2c
*Slave is same as a simple Bluetooth RC car*
