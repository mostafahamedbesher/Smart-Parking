
# Smart-Parking
Simple overview of use/purpose.

## Description

* Automate Entering And Exiting The Parking Through Unique ID for Each Car And Controlling Available Parking Spaces.
  Based on STM32f103c6 - ARM Cortex m3.



## How Smart-Parking Works

* First you must Enter Allowed Cars IDs and Save Them so they can access the parking later and this step is done only in the first use.
* Each car has its own ID which can access the parking gates using RFID card.
* The communications between RFID readers and STM32f103c6 are done using UART protocol.
* When a car wants to enter the gate, the driver should use his ID using RFID card and when the RFID reader reads it, it sends it to our MCU.
* Then MCU checks if the parking has available spaces and if true, then it checks the ID if it is Correct,It turn the green LED ON and opens the gate by moving Servo     motor to lift the barrier up.
* Then our MCU checks the PIR sensor Signal, if MCU gets High signal it means that the car is still not moving, so MCU doesnot return the barrier back.
* When the MCU doesnot get Signal From PIR sensor that means the car moved so in this case the MCU drives servo motor Back to The First Position To block The parking.
* The second case it might happens when entering wrong ID ,then the red LED turns on and firing the alarm.
* The same scenario happens with the exiting Gate.


https://user-images.githubusercontent.com/77936621/209366610-500f3600-6994-4d00-88bb-0c2e16da106c.mp4



## How Smart-Parking is Implemented

* I wrote Device Drivers For GPIO,RCC,UART,Timer on STMCubeIDE And put them in MCAL Layer, and also I wrote LCD and KeyPad Drivers And put them in HAL Layer.
  then I used These Drivers to Write My Application.




### Hardware

* STM32f103c6
* LCD 16x2
* Keypad 4x3
* Two RFID Card
* PIR sensor
* Two Servo Motors
* TWO LEDs



## Author And Contact Info

 Mostafa Hamed Besher  
 mostafahamed241@gmail.com
