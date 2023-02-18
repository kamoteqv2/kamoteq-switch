# kamoteq-switch
For Personal Use only | Not for Commercial

Tested on Arduino Uno | Esp8266 NodeMCU

***KamoteQ-switch Firmware Documentation***
The KamoteQ-switch firmware is a microcontroller board firmware that allows users to control the pins and perform various actions on the board using serial commands or the open source OpenHAB or Home Assistant smart home automation applications.

***How to use the KamoteQ-switch firmware:***

Flash the firmware onto the board using the appropriate flasher software (XLoader for Arduino Uno, NodeMCU flasher for ESP8266).
Connect the board to your desired circuit or device.


Alternatively, you can use the KamoteQ-switch firmware with OpenHAB or Home Assistant to control the board using their user interface.

## Integration with OpenHAB or Home Assistant:
### To use the KamoteQ-switch firmware with OpenHAB or Home Assistant, follow these steps:****

1. Install OpenHAB or Home Assistant on your desired device.
2. Add the KamoteQ-switch firmware as a new thing in your smart home automation application.
3. Once the new board is added as a thing, you can control the pins and perform various actions on the board using the OpenHAB or Home Assistant user interface.

## Integration with Serial Commands:
### To use the KamoteQ-switch firmware with serial commands, follow these steps:

1. Connect the board to your desired circuit or device.
2. Open the Arduino IDE software and navigate to the "Tools" menu. Select the appropriate board and port settings.
3. Open the Serial Monitor by clicking on the magnifying glass icon on the top right corner of the IDE window.
4. Set the baud rate to 115200.
5. Type in the desired serial commands for the KamoteQ-switch firmware in the Serial Monitor input box and press "Enter".
6. The firmware will receive the command and perform the necessary actions.

***Note:*** Refer to the available serial commands section for a list of commands you can use to control the board with serial commands.


### Available serial commands for Arduino:

- {"set":"erasepins"}: This command sets the board pin status all to default off or zero.
- {"devicename":"mydevicename"} update the device name
- {"dht":1} get the dht sensor values
- {"pinNum":<pinNumber>,"setMod":<pinMode>}: This command sets a specific pin on the microcontroller board to the desired state. Replace <pinNumber> with the pin number you want to set, and <pinMode> with the mode you want to set it to (e.g. "HIGH", "LOW").

***Note:*** There are a maximum of 16 output pins that can be used on the firmware for Arduino: D5-D19. Refer to the KamoteQ-switch firmware repository for the latest available commands and their descriptions.

### Available serial commands for ESP8266:

- {"erase":1} erase board information wifi and pins
- {"erasewifi":1} erase wifi credential
- {"erasepins":1} set pins to default 0
- {"ssid":"mywifi","password":"mypass"} update the wifi credential
- {"devicename":"mydevicename"} update the device name
- {"dht":1} get the dht sensor values
- {"erase":1}: This command erases the board pins and wifi password.
- {"erasewifi":1}: This command erases the wifi password.
- {"reset":1}: This command resets the ESP8266 board.
- {"pinNum":<pinNumber>,"setMod":<pinMode>}: This command sets a specific pin on the microcontroller board to the desired state. Replace <pinNumber> with the pin number you want to set, and <pinMode> with the mode you want to set it to (e.g. "HIGH", "LOW").

***Note:*** There are a maximum of 5 output pins that can be used on the firmware for ESP8266: GPIO 4, 5, 12, 13, 14. Refer to the KamoteQ-switch firmware repository for the latest available commands and their descriptions.
  
-------

***Credit:*** This application was developed by KMQ Tech TV (https://www.youtube.com/@kamoteqv2), a Youtube channel dedicated to teaching and promoting Free DIY technology.
