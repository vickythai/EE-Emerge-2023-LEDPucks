# Software Design
The capacitive sensing, puck communication, and game logic were programmed in C++ using the Arduino IDE and interfaced using the ESP32 board. 

## Capacitive Sense
We utilized the capacitive touch sensor embedded in the ESP32 microcontrollers to detect when someone is touching the puck. Capacitive sense relies on the change in capacitance, the ability for a system to store an electric charge, to detect when something is touched. In order to create a change, the electric charge in the system has to fluctuate, which is achieved when a conductive object, such as the player's hand, comes into contact with the sensor.

Along the inside rim of the puck, conductive tape is taped all around the inner lining and a wire is used to connect the tape to the sensor pins of the ESP32. A piece of acrylic is then placed on top of the tape to act as an insulator. All of these parts together allow the entire top area of the puck to act as the sensor.

## Puck Communication
The [painlessMesh](https://gitlab.com/painlessMesh/painlessMesh) library was used to support wireless communication between the pucks. This libary allows us to easily create a mesh network using ESP-MESH, a network protocol that allows multiple devices over a region of space to be connected with a WLAN (Wireless Local-Area Network). Communication between the ESP32s was implemented by broadcasting messages over the mesh network.

A master ESP32 was programmed to start and reset the game, as well as randomize which puck will turn on. Each puck contains it's own ESP32, which will communicate with the master to indicate if it's been pressed.

## Game Logic
Each individual puck corresponds to a certain number. When the game is started, a randomizer will pick a random number and check the status of the puck correponding to that number. If the puck is active, a different puck is chosen to turn on. 
