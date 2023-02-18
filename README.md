# kamoteq-switch
 For Personal Use only | Not for Commercial
 
 Tested on Arduino Uno | Esp8266 NodeMCU






Working with the serial monitor and sending serial commands can be a powerful tool when working with microcontrollers and other embedded systems. Here are the steps to follow:

Connect your microcontroller board to your computer via USB.
Open the Arduino IDE software and navigate to the "Tools" menu. Select the appropriate board and port settings.
Open the Serial Monitor by clicking on the magnifying glass icon on the top right corner of the IDE window.
Select the correct baud rate for your microcontroller board (usually 115200) in the dropdown menu at the bottom of the Serial Monitor window.
To send a command to the microcontroller, type the appropriate command in the Serial Monitor input box and press "Enter".
The microcontroller will receive the command and perform the necessary actions.
Alternatively, you can use a small serial monitor application called Termite. This application is included in the repository and can be downloaded and installed on your computer.

To erase the board pins and wifi password, type in the serial monitor {"set":"erase"}:

This command will erase all of the pin states and the WiFi password from the microcontroller board. The board will revert to its default state.

To erase the wifi password, type in the serial monitor {"set":"erasewifi"}:

This command will erase only the WiFi password from the microcontroller board.

To set the board pin status all to default off or zero, type in the serial monitor {"set":"erasepins"}:

This command will erase all of the pin states on the microcontroller board, setting them to their default off or zero state.

To reset the ESP8266 board, type in the serial monitor {"set":"reset"}:

This command will reset the ESP8266 microcontroller board.

To set specific pin status, type in the serial monitor {"pinNum":<pinNumber>,"setMod":<pinMode>}:

This command will set a specific pin on the microcontroller board to the desired state. Replace <pinNumber> with the pin number you want to set, and <pinMode> with the mode you want to set it to (e.g. "HIGH", "LOW"). This command can be used to turn a pin on or off. When the <pinMode> is set to "HIGH", the pin is set to a logic high voltage (typically 5 volts). When the <pinMode> is set to "LOW", the pin is set to a logic low voltage (typically 0 volts). Remember to set the baud rate to 115200.



***Credit:*** This application was developed by KMQ Tech TV (https://www.youtube.com/@kamoteqv2), a Youtube channel dedicated to teaching and promoting Free DIY technology.
