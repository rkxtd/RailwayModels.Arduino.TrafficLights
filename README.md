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
* connect arduino digital pins to diodes. each diode should be attached to resistor.
* updload the firmware to your arduino.
* have fun

## Signals and codes
![Red signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/red.png =21x106) - **Code: 0**

![Yellow signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/yellow.gif) - **Code: 1**

![Green signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/green.gif) - **Code: 2**

![Yellow/Green signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/yellow_green.png =21x106) - **Code: 3**

![Yellow/Yellow signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/both_yellow.gif) - **Code: 4**

![Yellow/Blinking Yellow signal](https://github.com/xcomanche/RailwayModels.Arduino.TrafficLights/blob/master/images/both_yellow_blinking.gif) - **Code: 5**
