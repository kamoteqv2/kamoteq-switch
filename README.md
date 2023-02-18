# KAMOTEQ-SWITCH
For Personal Use only | Not for Commercial

Tested on Arduino Uno | Esp8266 NodeMCU | Windows 8 and above

## KamoteQ-switch Firmware Documentation
The KamoteQ-switch firmware is a microcontroller board firmware that allows users to control the pins and perform various actions on the board using serial commands or the open source OpenHAB or Home Assistant smart home automation applications.

### How to use the KamoteQ-switch firmware:
Before using the KamoteQ-switch firmware, you need to connect the microcontroller board to your computer or laptop. Open the device manager to check the COM port number. If the device is not properly detected or the device driver for the board is missing, you can find the driver in the driver folder in the repository.

Once you have confirmed that the device is properly detected and the driver is installed, follow these steps:

1. Flash the firmware onto the board using the appropriate flasher software (XLoader for Arduino Uno, NodeMCU flasher for ESP8266).
2. Connect the board to your desired circuit or device. <click here for complete instruction>

## Integration with OpenHAB or Home Assistant:
### To use the KamoteQ-switch firmware with OpenHAB or Home Assistant, follow these steps:

1. Install OpenHAB or Home Assistant on your desired device.
2. Add the KamoteQ-switch firmware as a new thing in your smart home automation application.
3. Once the new board is added as a thing, you can control the pins and perform various actions on the board using the OpenHAB or Home Assistant user interface. <click here for complete instruction>

## Integration with Serial Commands:
### To use the KamoteQ-switch firmware with serial commands, follow these steps:

1. Connect the board to your desired circuit or device.
2. Open the Arduino IDE software and navigate to the "Tools" menu. Select the appropriate board and port settings.
3. Open the Serial Monitor by clicking on the magnifying glass icon on the top right corner of the IDE window.
4. Set the baud rate to 115200.
5. Type in the desired serial commands for the KamoteQ-switch firmware in the Serial Monitor input box and press "Enter".
6. The firmware will receive the command and perform the necessary actions.
  
Alternatively, if the Arduino serial monitor is not available, you can use the Termite serial monitor application, which is included in the repository. Once you have installed and run Termite, simply select the correct COM port number and set the baud rate to 115200. This will allow you to send and receive serial commands to the KamoteQ-switch firmware.


***Note:*** Refer to the available serial commands section for a list of commands you can use to control the board with serial commands.

### Available serial commands for Arduino:

#### Commands for erasing board information:  
- {"set":"erasepins"}: Sets all board pin statuses to the default "off" or "zero". In addition to using the serial command, board information can also be erased by placing a jumper wire between GPIO 13 and ground while the board is powered on. This will erase the board's pin and wifi settings.
- {"devicename":"mydevicename"}: Updates the device name to "mydevicename".
- {"dht":1}: Retrieves values from the DHT sensor.
  
#### Commands for controlling the board and updating settings:  
- {"pinNum":,"setMod":}: Sets a specific pin on the microcontroller board to the desired state. Replace the first value with the pin number you want to set, and the second value with the mode you want to set it to (e.g. "HIGH", "LOW").

#### Commands for getting board information:
- {"info":1}:   

***Note:*** There are a maximum of 16 output pins that can be used on the firmware for Arduino: D5-D19. Refer to the KamoteQ-switch firmware repository for the latest available commands and their descriptions.

### Available serial commands for ESP8266:

#### Commands for controlling the board and updating settings:
- {"erase":1}: This command erases the board's pin and wifi settings. In addition to using the serial command, board information can also be erased by placing a jumper wire between GPIO 13 and ground while the board is powered on. This will erase the board's pin and wifi settings.
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

#### Commands for getting board information:
- {"info":1}:   
  
***Note:*** There are a maximum of 5 output pins that can be used on the firmware for ESP8266: GPIO 4, 5, 12, 13, 14. Refer to the KamoteQ-switch firmware repository for the latest available commands and their descriptions.
  
-------

***Credit:*** This application was developed by KMQ Tech TV (https://www.youtube.com/@kamoteqv2), a Youtube channel dedicated to teaching and promoting Free DIY technology.
