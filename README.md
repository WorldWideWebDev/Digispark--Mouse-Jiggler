# Digispark--Mouse-Jiggler

// Written by James Franklin for Air-Gap in 2019
// www.air-gap.com.au

Create a mouse jiggler with Digispark ATtiny85 USB board

Requirements:

Digispark ATtiny85 USB development board or Good Copy which abundantley available  $1 -$10 

Arduino IDE Software  https://www.arduino.cc/en/Main/Software  Free

DIGISPARK Drivers  https://github.com/WorldWideWebDev/DigistumpArduino Free

Some Spare Time. 

Full Instructions here:-
http://digistump.com/wiki/digispark/tutorials/connecting

https://www.arduino.cc/en/Main/Software

https://github.com/digistump/DigistumpArduino/releases

https://raw.githubusercontent.com/digistump/arduino-boards-index/master/package_digistump_index.json


All info below from The Person who wrote this:-
https://air-gap.com.au/how-to-make-a-mouse-jiggler-with-digispark/


How to make a mouse jiggler with Digispark

On April 30, 2019, Posted by James , In General,Tips and Tricks, By Arduino,Digispark,Mouse Jiggler , With 9 Comments
Mouse jigglers are a useful tool in the IT field to keep a computer active for a wide range of purposes from stopping a screensaver activating in a presentation to preventing a computer shutting down for a forensic investigator.

There are two main categories of jigglers:

Software Jigglers: A computer program that is installed on the host which automatically moves the cursor at a set interval.
Pro’s: Cheap or Free, easily configurable, no extra circuitry
Cons: User may not be authorised to install software, easy to detect by IT department
Hardware jigglers: A device which tricks the operating system into thinking its a mouse.
An onboard micro-controller generates random or predefined movements
Pro’s: Plug & Play, No configuration, hard to detect, reliable
Con’s: Costs money, harder to reprogram
In this article we will be using a Digispark which is an affordable development board powered by a ATtiny85 micro-controller running at 16MHZ with 6K usable flash which can communicate with a host over USB. These boards are incredibly capable and can be used for a wide range of tasks including injecting keystrokes and mouse movements.

 

When you get your Digispark it will look similar to the picture, for this project we will not be using header pins and we will be programming the device through USB.

The first step of programming the Digispark is downloading the latest Arduino programming IDE.
https://www.arduino.cc/en/Main/Software
arduino download page
Next is downloading and installing the Digispark drivers. You may need to accept multiple notifications through the install process.
https://github.com/digistump/DigistumpArduino/releases
Once both the Arduino IDE and Digispark drivers have been installed, add the digispark JSON configuration file to the IDE. This is done by opening the Arduino IDE, clicking on ‘File, Preferences’ and adding the following URL into the ‘Additional Boards Manager URL’s’ box, then click ‘OK’.
https://raw.githubusercontent.com/digistump/arduino-boards-index/master/package_digistump_index.json


Once installed, go-to Tools –> Board and select “Board Manager

In the top left hand corner change the Type to “Contributed” and click the install button on the “Digistump AVR Boards by Digistump package”. This will allow the Arduino IDE to program the Digispark controllers.

Once installed, go-to Tools –> Board and select “Digispark – Default 16.5mhz”. This set’s the IDE to compile the code for the Digispark board.

Next go-to, Tools –>Programmer and set it as “USBtinyISP”

We have created an opensource simple Mouse Jiggler sketch (program) for the Digispark v3 which moves the cursor every 10-30 seconds in a square pattern. Download and open it in Arduino IDE.
Download: MouseJiggler.ino
Click on the “Upload” button to compile the sketch and upload it to the Digispark.

If successful, you should now see the Digispark flash every 10-30 seconds to indicate a ‘mouse jiggle’. The mouse movement should be near undetectable.
 

