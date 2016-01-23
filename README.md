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
[[images/red.PNG|alt=Red]] - Red signal. *Code: 0000*. Road is closed.
[[https://upload.wikimedia.org/wikipedia/ru/f/f1/Main_approach.gif|alt=Top Yellow]] - Yellow Signal
[[https://upload.wikimedia.org/wikipedia/ru/f/f1/Main_approach.gif|alt=Green]] - Yellow Signal