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

## Part 1: Introduction to the module

The following introductory slideshow will be presented by Jay during the opening class. It provides an overview of the module, its components, expectations, and deliverables. 

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRGF9iiknpFD8UbYc0AZwdgcNO8SvpcMJ73Y5ASyecBScyvJuylV-xTP95J_hA42YNe1FkxRFMuXxhE/embed?start=false&loop=true&delayms=15000" frameborder="0" width="640" height="389" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

<br>
[View slides in PDF format](slides.pdf)
<br>


## Part 2: Intro to Arduinos, Sensors, and Actuators

Follow along with this short presentation of the types of electronic components we'll be using in this module. Feel free to unpack your kit and check out the components.

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRGF9iiknpFD8UbYc0AZwdgcNO8SvpcMJ73Y5ASyecBScyvJuylV-xTP95J_hA42YNe1FkxRFMuXxhE/embed?start=false&loop=true&delayms=15000" frameborder="0" width="640" height="389" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>


## Part 3: Getting Started
Now that you've unpacked your kit, it's time to plug in your Arduino and begin using it. 
### Physically connect the Arduino
- The Arduino can use the USB port to communicate with your computer, as well as draw power from is. Use the USB cable provided to connect the Arduino to your computer's USB port. If done correctly, the on-board LED labeled "**ON**" should light up. If this doesn't work, disconnect and attempt again. 
- Depending on what program was uploaded to your Arduino board last, you may or may not see the on-board LED lalebeled "**L**" light up or flash. Arduinos will run its uploaded program upon power-up, and will continue to do so until the *reset* button is pressed, the power is disconnected, or the board breaks. 
  - Note that the on-board LED lalebeled "**L**" is connected to digital input/output (IO) pin number 13; if the current program provides instructions for current to be provided to pin 13, it'll be reflected in the on-board LED (whether or not anything is connected to digital pin 13. 
  
### Open the Arduino IDE; Connect to the Arduino board
Once your Arduino is physically connected to your computer, open up the Arduino IDE program. A new sketch window will appear. The sketch window contains a number of different areas, which are labeled below. You'll learn and use these functions througout the module.

![Arduino IDE with parts labeled](images/arduino-ide.png "The Arduino IDE")

Depending on your operating system, your Arduino may or may not be connected via a serial port (which allows for communication between the computer and the Arduino). 
- You can check the status of your connection by clicking on >Tools>Port. 

A physically connected Arduino should appear in the Serial Ports list as **COMX (Arduino UNO)** as shown below:

![Arduino IDE with Ports window showing](images/arduino-port1.png "Arduino IDE Ports list -- Arduino not connected")

To establish the serial connection, click on the listed COM port that where the Arduino is connected. A checkmark should appear beside the port when a connection has been made.
![Arduino IDE with Ports window showing](images/arduino-port2.png "Arduino IDE Ports list -- Arduino connected")

## Part 4: Uploading and running a program

### Open the program "Blink"
In this exercise, you are going to upload your first program to the Arduino. For this case, we'll use one of the example programs that come with the Arduino IDE.
- Go to >File>Examples>0.1Basics> and click on **Blink**. This will open up a new sketch (what Arduino calls its programs) with the Blink program. 

![Arduino IDE showing the blink program](images/opening-blink.png "Opening blink in the Arduino IDE")

### Upload "Blink" to the Arduino
- Ensuring that the Arduino is connected (both physically and through the COM port), click the upload button. 
  - The status window should first indicate that it is *Compiling sketch*, and then indicate that it is *Uploading*.
- If the upload was succesful, the status window will indicate *Done uploading*, and the info window will communicate the following (or similar):
```
Sketch uses 924 bytes (2%) of program storage space. Maximum is 32256 bytes.
Global variables use 9 bytes (0%) of dynamic memory, leaving 2039 bytes for local variables. Maximum is 2048 bytes.
```
- If an error occurs, the status window will provide a general error message, and the info window will give additional information on it (you may need to scroll to see it). 
  - If the error occurred when uploading (i.e. a connection couldn't be made between the computer and the Arduino), the status window will read: *An error occurred while uploading the sketch*. 
  - If the error occurred when compiling the code (i.e. there's something wrong with your code), the status window will provide an error message, and the problematic line will be highlighted in the sketch. 

## Part 5: Understanding an Arduino sketch
The blink sketch provides a good opportunity to explore the three fundamental elements of an Arduino sketch. 

### The commented preface
![Arduino blink sketch comments](images/blink-comment.png "Blink sketch comments")

The opening, grey-text section of the sketch is a block comment that contains human-readable information about the program. This section is ignored by the Arduino compiler, and its sole purpose is to provide humans (whether yourself or others) with more information on the code. Comments can be inserted into a sketch as a block using the ```/*``` and ```*/``` characters around the commented text, e.g:
```
/* 
All of this is 
a comment
*/
```

Comments are an important part of writing and maintaining computer code, as it's often much easier to understand what the code is doing when there is plain, human-readable text accompanying it. It's also important to record your changes over time. Additionally, you can use comments to temporarily remove certain lines of code that you don't want to be executed.

A good commented preface should contain some/all of the following information:
- What the code does.
- A description (or link to a diagram) of the circuit that it works alongside. 
- Links to any other information.
- Who created it, revised it, and when this was done.
- Information on licensing / rights on the code.


You'll also notice later in the sketch that comments are inserted on single lines (whether at the start or end) using the ```//``` characters: 
```
// This is a commented line
```

### The setup function
![Arduino blink sketch setup function](images/blink-setup.png "Blink sketch setup function")

As mentioned in the comment above it, the setup function runs a single time when the board is turned on, reset, or when a new program is uploaded to it. The purpose of the setup function is to declare constants and run commands that configure the Arduino board to operate as desired in the following loop function. 

Note the general structure of a function used for the setup function (and other functions):

```
<returned_value> <name of function> (<input values>){
first command; //commands end with a semicolon
second command;
third command;
...
} // curly braces contain the commands at the top and bottom
```

In this casee, there is no returned value (the term ```void``` is used to indicate this), the name of the function is *setup*, there are no input values (thus the empty parentheses), and there is only one command executed.

#### Q1: 
- In this example, the only command executed in the setup function is ```pinMode(LED_BUILTIN, OUTPUT);```. What does this line do? 

#### A1: 
- ```pinmode``` is a built-in function that allows you to determine whether a given digital pin should be *INPUT* (receives current) or *OUTPUT* (delivers current). 
- The first *argument* to the function, ```LED_BUILTIN``` is a built-in constant that refers to digital pin 13, which is connected to the built-in LED on the Arduino board (labelled **"L"**). Note that you could replace ```LED_BUILTIN``` with ```13``` and it would work just the same. 
- The second *argument*, ```OUTPUT```, indicates that digital pin 13 should be set to output current.

### The loop function
![Arduino blink sketch setup function](images/blink-loop.png "Blink sketch loop function")

As also indicated in the preceding comment, the loop function will run repeatedly for as long as the Arduino board is powered and operational.

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
































