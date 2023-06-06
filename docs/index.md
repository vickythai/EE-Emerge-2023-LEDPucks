# LED Pucks

LED Pucks is an interactive project created by a team of UC Davis [EE-Emerge](https://ece.ucdavis.edu/ee-emerge) students. Inspired by the popular arcade game, Whack-a-mole, the project featues multiple devices that communicate over a wireless mesh network. Together, these devices form a fun and interactive game that utilizes capacitive touch sensors and colorful LED lights. The goal of the game is to tap the various pucks when their LEDs turn on in order to turn them off and accumulate the most points within a time limit. 

# About the Project:

LED Pucks was designed to be an interactive way to showcase the power and creativity of electronics. With the wireless feature of the pucks, they can be placed anywhere within a 50ft radius, encouraging people to run around to hit the various pucks. We used [ESP32](https://www.espressif.com/en/products/socs/esp32) microcontrollers, which have Wi-Fi capabilities that allow us to control the pucks wirelessly. We collected user input through [capacitive sensing](https://en.wikipedia.org/wiki/Capacitive_sensing) by placing a piece of acrylic on copper tape, which is wired to the ESP32. Lined along the inside of the puck are [NeoPixel RGB LED strips](https://www.adafruit.com/product/1138) that light up and change colors to indicate which puck to hit. All of these parts are housed in a custom designed two-part enclosure that features a friction-fitted body and lid.

<img src="https://github.com/vickythai/EE-Emerge-2023-LEDPucks/blob/main/pictures/puck_breakdown.png?raw=true" alt="Puck Breakdown" width="40%" height="40%"/>
