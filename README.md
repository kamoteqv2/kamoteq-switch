# kamoteq-switch
For Personal Use only | Not for Commercial

Tested on Arduino Uno | Esp8266 NodeMCU

## KamoteQ-switch Firmware Documentation
The KamoteQ-switch firmware is a microcontroller board firmware that allows users to control the pins and perform various actions on the board using serial commands or the open source OpenHAB or Home Assistant smart home automation applications.

### How to use the KamoteQ-switch firmware:

1. Flash the firmware onto the board using the appropriate flasher software (XLoader for Arduino Uno, NodeMCU flasher for ESP8266).
2. Connect the board to your desired circuit or device.

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

- {"set":"erasepins"}: Sets all board pin statuses to the default "off" or "zero".
- {"devicename":"mydevicename"}: Updates the device name to "mydevicename".
- {"dht":1}: Retrieves values from the DHT sensor.
- {"pinNum":,"setMod":}: Sets a specific pin on the microcontroller board to the desired state. Replace the first value with the pin number you want to set, and the second value with the mode you want to set it to (e.g. "HIGH", "LOW").
***Note:*** There are a maximum of 16 output pins that can be used on the firmware for Arduino: D5-D19. Refer to the KamoteQ-switch firmware repository for the latest available commands and their descriptions.

### Available serial commands for ESP8266:

#### Commands for controlling the board and updating settings:
- {"erase":1}: This command erases the board's pin and wifi settings.
- {"erasewifi":1}: This command erases the wifi settings.
- {"reset":1}: This command resets the ESP8266 board.
- {"pinNum":,"setMod":}: This command sets a specific pin on the board to the desired state. Replace with the pin number you want to set, and with the mode you want to set it to (e.g. "HIGH", "LOW").
- {"ssid":"mywifi","password":"mypass"}: Use this command to update the wifi settings with your network name and password.
- {"devicename":"mydevicename"}: Use this command to update the device name.
- {"dht":1}: Use this command to get the DHT sensor values.
#### Commands for erasing board information:
- {"erase":1}: This command erases the board's pin and wifi settings.
- {"erasewifi":1}: This command erases the wifi settings.
- {"erasepins":1}: This command sets all pins to default 0.

***Note:*** There are a maximum of 5 output pins that can be used on the firmware for ESP8266: GPIO 4, 5, 12, 13, 14. Refer to the KamoteQ-switch firmware repository for the latest available commands and their descriptions.
  
-------

***Credit:*** This application was developed by KMQ Tech TV (https://www.youtube.com/@kamoteqv2), a Youtube channel dedicated to teaching and promoting Free DIY technology.
