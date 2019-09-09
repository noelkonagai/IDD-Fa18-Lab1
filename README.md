# Lab1: Blink!

**A lab report by Noel Konagai**

## Part A. Set Up a Breadboard

![Breadboard Setup](https://github.com/noelkonagai/interactive-devices/blob/master/Lab%201/breadboard_setup.jpeg "Breadboard Setup")

## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**

From left to right: brown (1), black (0), black (0), black (x1).
 
**b. What do you have to do to light your LED?**

I needed to connect a power source (i.e. the USB cable to my computer) in order to light the LED. I also needed to press the switch once the Arduino board was connected to my laptop.

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**

No lines of code needed to be changed.

**b. What line(s) of code do you need to change to change the rate of blinking?**

The delay needed to be changed.

**c. What circuit element would you want to add to protect the board and external LED?**

A current-limiting resistor serially connected to the LED light.
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**

Around 10ms. To prove to myself that it is still blinking, I logged the behavior in the loop by adding `Serial.print("high \n")` and `Serial.print("low \n")`.

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**

[Link to code](https://github.com/noelkonagai/interactive-devices/blob/master/Lab%201/blink_led.ino)

### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[Link to LED blinking Video](https://youtu.be/PW_FK2ckymU)

## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**

I was able to get the LED to glow through the turning range of the potentiometer. I used a 10kOhm resistor as I didn't have a 220 Ohm resistor.

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**

`int led` needed to be changed to 11.

**b. What is analogWrite()? How is that different than digitalWrite()?**

`analogWrite()` enables me to send a signal that is continuous. `digitalWrite()` would only allow me to send `HIGH`, which in this case is 5V or `LOW`, which is GND as a signal.

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside.

![Shaver Schematic](https://github.com/noelkonagai/interactive-devices/blob/master/Lab%201/IDD%20Lab%201%20-%20Shaver%20Circuit.png "Shaver Schematic")

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

My beard trimmer has a switch, and I would argue that it is not a computation.

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

My beard trimmer has no sensors.

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

My beard trimmer is battery powered. It uses a 1.2V battery, which can be charged through a charging cable. Unfortunately, I no longer have the cable, but it certainly had a power regulation function.

**d. Is information stored in your device? Where? How?**

My beard trimmer does not store information.

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

I decided to cut off the motor and replace it with an LED and a resistor. However, since my battery was only 1.2V the LED did not light up. This is why, I decided to connect serially the 1.2V battery with my Arduino 5V source as shown in my video. I used alligator clips for the two ends of the original circuit where the motor used to be to connect it with the source and GND of the breadboard circuit. I also moved back the LED and resistor to the breadboard to use fewer jumper wires. This way I was able to light up the LED and it was very bright (because of the additional 1.2 V).

### 3. Build your light!

[Link to Frankenlight Video](https://youtu.be/_W9P18gkYeU)
