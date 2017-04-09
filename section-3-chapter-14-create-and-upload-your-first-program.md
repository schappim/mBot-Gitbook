# Section 3

---

## Chapter 15: Create and upload your first program

---

In this chapter you will learn about:

* How to create a new Scratch program
* How to program the mBot using Scratch instructions
* What is an "Arduino board"
* What is the "Arduino Program" and how it corresponds to the "Scratch Program"
* How to upload a program to the mBot
* How to set the LEDs on the mBot to any colour

---

We can move on to doing some actual playing around with the mBot using mBlock, now.

On the right bottom corner of the Scripts tab \(1\) you will find the "Robots" group of blocks \(2\). Once you select it, there's an mBot section \(3\) which contains all of the different programming blocks that we can use with the mBot.

![](/assets/Img.3.15.1.jpg)

\[Image 2.15.1: The mBot instruction blocks on the Scripts tab\]

Let's have a quick look at some of these instruction blocks.

The first one, for example, reads "run forward at speed 0". Clicking on it, we can change that to backwards, right or left, at a particular speed.

There's one that allows us to set the onboard LEDs at a specific colour.

One for taking decisions when the onboard button is pressed and lots of other blocks for programming behaviour to the mBot.

### Instructions for basic and additional components

Out of the box, the mBot comes with a number of capabilities based on sensors or motors or other attachments like, for example:

* an ultrasonic sensor
* an infrared sensor
* a line follower module
* a light intensity sensor

As far as outputs and actuators are concerned, there are:

* two motors connected to two individual ports: one for each motor
* two RGB LEDs

Apart from these basic capabilities, though, we can purchase and plug onto the mBot additional components and eventually make use of the mBlock extension to interact with them. So, for example, we can purchase a sound sensor separately and use the corresponding mBlock instruction block to interact with it. A sound sensor is practically a microphone and we can clap, for example, and get the mBot to react to that clapping.

We can have a 3-axis gyroscope, too, which is very good for detecting a change in direction like when the robot turns over, upside-down.

For this crash course on the mBot though, we will be focusing on the capabilities that the mBot comes with out of the box without any additional components.

### Creating a new program

In order to create a new mBlock program we go to menu "File" and click on "New". In the "Scripts" tab, in "Robots", we pick the "mBot Program" header block and drag and drop it into the scripts area. Every mBot program must start with this block.

Below it, we can attach other blocks that fit. For example, let's say that we would like to change the colour of the two onboard RGB LEDs. To do that, we pick the "set led on board..." instruction block and drag and drop it and connect it to the mBot header. Thereafter, we can configure it further by choosing which one of the two LEDs we would like to manipulate \(left/right/both\) and what colour to set by choosing values from 0 to 255 for all three red/green/blue attributes. Through the combination of these three, we can create all kinds of other composite colours. For our example let's just choose to turn on "all" LEDs and let's pick 255 for red and 0 \(zero\) for both green and blue. That should give a plain red colour to both the on-board LEDs.

![](/assets/Img.3.15.2.jpg)

\[Image 2.15.2: A small program that will turn all LEDs to red\]

Once finished with our program we must connect the USB cable to the USB port \(1\) on the mBot. We will know that the connection has taken place because there wil be a red LED \(2\) which indicates that we've got power from the USB. But that's not enough power to power up the robot. Once we plug in the cable, we need to turn on the robot by flipping the switch \(3\) to on and then the robot will be ready to be programmed.

![](/assets/Img.3.15.3.jpg)

\[Image 2.15.3: Connecting the USB on the mBot\]

The next step is to go to the "Connect" menu and look for the serial port \(a COM port\) where the mBot is connected to the computer. It is always going to be a port that has a number larger than one. That is because COM1 is typically used by the operating system itself. In our example the port to which the mBot is connected happens to be COM4.

![](/assets/Img.3.15.4.jpg)

\[Image 2.15.4: Connecting to the Serial Port\]

Next, we right-click on the mBot program and choose "Upload to Arduino".

**Note**: Some people get confused about this, thinking "What's the Arduino? I'm just trying to program my mBot!" Well, inside the mBot there is an Arduino board and that's where the program is loaded.

By doing that we get to see the uploading component of the mBlock application. What we see there is the translation of the simple Scratch-based program in an Arduino program or "sketch" as we call it. We notice that we've got a lot of instructions there. Most of it is just the infrastructure for supporting the functionality that we've selected in the mBot program.![](/assets/Img.3.15.5.jpg)\[Image 2.15.5: The Scratch block corresponding to Arduino instructions\]

We want our mBot to just turn the two LEDs into red and the program shown above does just that: line 34 sets the colour to red and line 35 turns the LEDs on. Everything else that we see around is just in support of these two lines of instructions.

If we experiment further and drop some other block into the program, we will notice that another instruction is going to appear somewhere in the Arduino program. If we change the order of the instruction blocks, we are going to see that the Arduino instructions are going to change, accordingly.

And that is how mBlock makes programming easy: it provides a graphical interface for the programmer where instruction blocks are just picked, dragged and dropped instead of typing traditional text-based instructions.

So, we can actually ignore the Arduino program and just click on the "Upload to Arduino" button that will transfer the program to the mBot.

**Note**: If the message "Please connect the serial port." appears, we just need to go to: menu Connect &gt; Serial Port and click on the right COM port. The message does not refer to a physical cable connection!

If all goes well and the uploading starts, we should see a lot of text flowing through. What happens is that mBlock "compiles" the Arduino program, using an embedded compiler. That means that the text program is being translated into binary \(a long string of zeros and ones\) which is the only programming format the Arduino can actually understand.

After the program uploads, we should be able to see the two LEDs shine red.

Let's try a variation of the program now and have the right LED shine green and the left LED shine blue.

**Note**: Click on "Back" if you'd like to close the view of the Arduino program.

![](/assets/Img.3.15.6.jpg)\[Image 2.15.6: A program for setting two different colours. On the left in Scratch blocks, on the right in Arduino text.\]

Drag and drop blocks and change parameters until you have the program shown in the image above. Right click on the program and "Upload to Arduino". You should be able to see, now, the mBot LEDs shining in accordance with the instructions: left one green, right one blue.

From here on, we can play some more and experiment with different colour value combinations. Remember that we are not confined to using the values from the drop-down. We can actually go and change that to any value between 0 and 255.

**Note**: To find the value for the Red, Green and Blue components of any colour, Google for "colour chooser" or "colour wheel"

### Questions

Question 3.15.1: Does a light sensor belong to the basic pack or is it an additional component?

A. Basic pack.

B. Additional component.

_Answer: B_

Question 3.15.2: What does an Arduino board have to do with the mBot?

A. It is an additional component.

B. Nothing really.

C. It is inside the mBot and it is actually where the program is loaded.

D. It is the part of the screen where the text program appears.

_Answer: C_

Question 3.15.3: In what format is the program actually uploaded to the mBot?

A. In binary \(zeros and ones\)

B. In Arduino text

C. In Scratch blocks

D. It doesn’t get uploaded but rather executed on the computer

Answer: A

Question 3.15.4: Fill in the RBG values of the colour known as “cornflower blue”? \(Hint: search on the internet for it\)

R = \_\_\_\_\_\_\_\_ G = \_\_\_\_\_\_\_\_ B = \_\_\_\_\_\_\_\_

Answer: R = 100 G = 149 B = 237

