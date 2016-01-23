# Controlling Railway trafic light using Arduino.
## Block system
To make controlling of a layout easy and not depending on DCC (which is hell in terms of controlling anything except Trains) i decided to move the logic to Arduino.
Nano version you could buy for 3$ on an Ebay. What makes integration of Traffic Lights - super-easy and cheap.
To have fully operational piece you will need just:
* arduino Nano
* 8 diods (3 yellow, 1 red, 1 green, 1 green diod bar, 1 white, 1 blue)
* 8 resistors (82 OM)
* wires

## Scheme
* connect arduino digital pins to diodes. each diode should be attached to resistor. Detailed instructions, which pins should be attached to which diodes could be found in USSRRailwayTrafficLight/USSRRailwayTrafficLight.ino sources.
* updload the firmware to your arduino.
* have fun

## Plans
Right now i'm working on arduino network. Where For each Railway block (logical unit) will corresponds one Arduino DUO, with connections to Slave Aruino network Using I2C protocol.
So in fact, that one controller will be responsible for all the things happening inside the block.
Using I2C protocol we could connect 127 devices to One Arduino Duo. And for main controller, to communicate between signal nodes, will have to send only 4 bits of data.

## Signals and codes
![Red signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/red.png) - **Code: 0**

![Yellow signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/yellow.gif) - **Code: 1**

![Green signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/green.gif) - **Code: 2**

![Yellow/Green signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/yellow_green.png) - **Code: 3**

![Yellow/Yellow signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/both_yellow.gif) - **Code: 4**

![Yellow/Blinking Yellow signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/both_yellow_blinking.gif) - **Code: 5**

![Blinking Yellow signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/yellow_blinking.gif) - **Code: 6**

![Yellow/Yellow/Green bar signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/both_yellow_green_bar.gif) - **Code: 7**

![Yellow/Blinking Yellow/Green bar signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/both_yellow_blinking_green_bar.gif) - **Code: 8**

![Blinking Green/Yellow/Green bar signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/green_blinking_yellow_green_bar.gif) - **Code: 9**

![Blinking Green](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/green_blinking.png) - **Code: 10**

![Yellow/White](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/yellow_white.gif) - **Code: 11**

![Green/White](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/green_white.gif) - **Code: 12**

![Yellow Blinking/White](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/yellow_blinking_white.gif) - **Code: 13**

![Blue](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/blue.png) - **Code: 14**

## Demo:
[![Automatic mode](http://img.youtube.com/vi/5f4s45Dhabo/0.jpg)](https://www.youtube.com/watch?v=5f4s45Dhabo)
