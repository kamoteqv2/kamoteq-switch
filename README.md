# kamoteq-switch
 For Personal Use only | Not for Commercial
 
 Tested on Arduino Uno | Esp8266 NodeMCU


### KamoteQ-switch Firmware Documentation

The KamoteQ-switch firmware is a microcontroller board firmware that allows users to control the pins and perform various actions on the board using serial commands.

***How to use the KamoteQ-switch firmware:***

1. Flash the firmware onto the board using the appropriate flasher software (XLoader for Arduino Uno, NodeMCU flasher for ESP8266).
2. Connect the board to your desired circuit or device.
3. Open the Arduino IDE software and navigate to the "Tools" menu. Select the appropriate board and port settings.
4. Open the Serial Monitor by clicking on the magnifying glass icon on the top right corner of the IDE window.
5. Set the baud rate to 115200.
6. Type in the desired commands for the KamoteQ-switch firmware in the Serial Monitor input box and press "Enter". The firmware will receive the command and perform the necessary actions.

***Available commands:***

- {"set":"erase"}: This command erases the board pins and wifi password.
- {"set":"erasewifi"}: This command erases the wifi password.
- {"set":"erasepins"}: This command sets the board pin status all to default off or zero.
- {"set":"reset"}: This command resets the ESP8266 board.
- {"pinNum":pinNumber,"setMod":pinMode}: This command sets a specific pin on the microcontroller board to the desired state. Replace <pinNumber> with the pin number you want to set, and <pinMode> with the mode you want to set it to (e.g. "HIGH", "LOW").
 
***Note***: Refer to the KamoteQ-switch firmware repository for the latest available commands and their descriptions.

-------

***Credit:*** This application was developed by KMQ Tech TV (https://www.youtube.com/@kamoteqv2), a Youtube channel dedicated to teaching and promoting Free DIY technology.
