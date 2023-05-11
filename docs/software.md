# Software Design
The capacitive sensing, puck communication, and game logic were programmed in C++ using the Arduino IDE and interfaced using the ESP32 board. 

# Capacitive Sense

# Puck Communication
The [painlessMesh](https://gitlab.com/painlessMesh/painlessMesh) library was used to support wireless communication between the pucks. This libary allows us to easily create a mesh network using ESP-MESH, a network protocol that allows multiple devices over a region of space to be connected with a WLAN (Wireless Local-Area Network). Communication between the ESP32s was implemented by broadcasting messages over the mesh network.

A master ESP32 was programmed to start and reset the game, as well as randomize which puck will turn on. Each puck contains it's own ESP32, which will communicate with the master to indicate if it's been pressed.

# Game Logic

