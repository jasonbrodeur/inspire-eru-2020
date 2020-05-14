# ERU - Day 1 Worksheet

**Welcome to Electronics for the Rest of Us!**  
<br>

Thanks for being a part of this module. Over the next four days, we'll be working together to explore some fundamental concepts in electronics, programming, and version control--all while building some small but interesting devices! 

This module assumes no prior knowledge or experience with electronics or programming--we'll start simple and see how far we get!

This module will use a mix of asynchronous and synchronous activities, which will (hopefully) allow you to work at your own pace (and on your own schedule), while interacting with, supporting, and getting support from me and your peers. All of the materials for this module will be provided to you in both written and video formats--all of which will be presented on these webpages. For communication purposes, we'll use Microsoft Teams.  

## Learning Objectives
By the end of this module, you will be able to:  
- Explain the fundamental concepts and operational principles of simple circuits, sensors and actuators
- Apply fundamental principles to build simple circuits that interact with their surrounding environments
- Create and modify software code to control the device and create comments to document its functionality
- Apply your skills, knowledge and creativity in the process of creating an original electronic device
- Use Markdown to format text in a simple yet effective manner
- Create, edit, and version control files in a GitHub repository
- Use GitHub Pages to share your results on an openly-accessible webpage

## Day 1, Part 1: Introduction to the module

The following introductory slideshow will be presented by Jay during the opening class. It provides an overview of the module, its components, expectations, and deliverables. 

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRGF9iiknpFD8UbYc0AZwdgcNO8SvpcMJ73Y5ASyecBScyvJuylV-xTP95J_hA42YNe1FkxRFMuXxhE/embed?start=false&loop=true&delayms=15000" frameborder="0" width="640" height="389" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

<br>
[View slides in PDF format](slides.pdf)
<br>


## Day 1, Part 2: Intro to Arduinos, Sensors, and Actuators

Follow along with this short presentation of the types of electronic components we'll be using in this module. Feel free to unpack your kit and check out the components.

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRGF9iiknpFD8UbYc0AZwdgcNO8SvpcMJ73Y5ASyecBScyvJuylV-xTP95J_hA42YNe1FkxRFMuXxhE/embed?start=false&loop=true&delayms=15000" frameborder="0" width="640" height="389" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>


## Day 1, Part 3: Getting Started
Now that you've unpacked your kit, it's time to plug in your Arduino and begin using it. 
### 1.3a Physically connect the Arduino
- The Arduino can use the USB port to communicate with your computer, as well as draw power from is. Use the USB cable provided to connect the Arduino to your computer's USB port. If done correctly, the on-board LED labeled "**ON**" should light up. If this doesn't work, disconnect and attempt again. 
- Depending on what program was uploaded to your Arduino board last, you may or may not see the on-board LED lalebeled "**L**" light up or flash. Arduinos will run its uploaded program upon power-up, and will continue to do so until the *reset* button is pressed, the power is disconnected, or the board breaks. 
  - Note that the on-board LED lalebeled "**L**" is connected to digital input/output (IO) pin number 13; if the current program provides instructions for current to be provided to pin 13, it'll be reflected in the on-board LED (whether or not anything is connected to digital pin 13. 
  
### 1.3b Open the Arduino IDE; Connect to the Arduino board
Once your Arduino is physically connected to your computer, open up the Arduino IDE program. A new sketch window will appear. The sketch windows contains a number of different areas--their functions are shown below:

![Arduino IDE with parts labeled](images/arduino-ide.png "The Arduino IDE")





Depending on your operating system, your Arduino may or may not be connected via a serial port (which allows for communication between the computer and the Arduino). 
- You can check the status of your connection by clicking on >Tools>Port. 

A physically connected Arduino should appear in the Serial Ports list as **COMX (Arduino UNO)** as shown below:

![Arduino IDE with Ports window showing](images/arduino-port1.png "Arduino IDE Ports list -- Arduino not connected")

To establish the serial connection, click on the listed COM port that where the Arduino is connected. A checkmark should appear beside the port when a connection has been made.
![Arduino IDE with Ports window showing](images/arduino-port2.png "Arduino IDE Ports list -- Arduino connected")

### Day 1, Part 4: Uploading and running a program

In this exercise, you are going to upload your first program to the Arduino. For this case, we'll use one of the example programs that come with the Arduino IDE.
- Go to >File>Examples>0.1Basics> and click on **Blink**. This will open up a new sketch (what Arduino calls its programs) with the Blink program. 
- Ensuring that the Arduino is connected (both physically and through the COM port), 


![Arduino IDE showing the blink program](images/opening-blink.png "Opening blink in the Arduino IDE")



## Resistors 
Use the attached image to answer the following questions: 
Q1. What colour code would be found on a 10 Kohm (10000 ohm) resistor using: 
- Four bands?
- Five bands?

A1. Use [resisto.rs](http://resisto.rs/) to assess your answer (enter ```10K``` into the box). A resource like [resisto.rs](http://resisto.rs/) is useful when you have a desired resistance and want to know the colour code.

Q2. Identify the 10 Kohm resistors in your kit
- Hint: there may be a mix of 4- and 5-band codes used

Q3. Use the colour code chart to identify the resistance of the other resistors in your kit (hint: the rest all have the same resistance and all use a 4-band colour code).

A3. Use a resistor colour code calculator like [this](https://www.digikey.ca/en/resources/conversion-calculators/conversion-calculator-resistor-color-code-4-band) to assess your answer. These kind of calculators are useful when you have a resistor in hand (i.e. you know the colour code), and need to know its resistance.



