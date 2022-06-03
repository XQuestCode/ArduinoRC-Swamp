# ArduinoRC-Swamp
Communication between two RC controlled car using 3 HC05 modules
**Instructions on binding HC05 to the slave's HC05**
<br>a. Connect slave to the the aruino, upload a new sketch. [here](https://pastebin.com/WQsq0igT)</br>
<br>b. Connect Rx pin to Rx of arduino and Tx to Tx of arduino.</br>
<br>c. go to AT mode of HC05 (_hold button for few seconds while powering up, result in slow blinks_)</br>
<br>d. Open serial monitor, set the baud rate to 38400.</br>
<br>e. Type **AT** to check if everything is correct (results an OK reply)</br>
<br>f. Type **AT+ADDR?** (result in something like **+ADDR:0019:10:08FED3** )</br>
<br>g. Now unplug this HC05, and connect the Master HC05.</br>
<br>h. Go to AT mode.</br>
<br>i. Type **AT+ROLE=1**</br>
<br>j Type **AT+BIND = 0019,10,08FED3** (your slave address)</br>
<br>k. Good to go, power them seperately, and they are ready to be binded</br>


<br>
#Instructions on making Bluetooth controlled RC car
https://github.com/XQuestCode/Arduino-Bluetooth-RC-car
</br>
<br>
[Video guide}(https://youtu.be/pGfxNgYMi2c)
</br>
*Slave is same as a simple Bluetooth RC car*
