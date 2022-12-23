
# Smart-Parking
Simple overview of use/purpose.

## Description

Automate Entering And Exiting The Parking Through Unique ID for Each Car And Controlling Available Parking Spaces.
Based on STM32f103c6 - ARM Cortex m3


## How Smart-Parking is Implemented

First I wrote Device Drivers For GPIO,RCC,UART,Timer And put them in MCAL Layer, and also I wrote LCD and KeyPad Drivers And put them in HAL Layer.
then I used These Drivers to Write My Application.


## How Smart-Parking Works




### Hardware

* STM32f103c6
* LCD 16x2
* Keypad 4x3
* Two RFID Card
* PIR sensor
* Two Servo Motors



## Author And Contact Info

 Mostafa Hamed Besher  
 mostafahamed241@gmail.com
