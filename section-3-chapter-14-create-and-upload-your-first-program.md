# Section 3

---

## Chapter 15: Creating and uploading our first program

---

In this chapter you will learn about:

* How to create a new Scratch program
* How to program the mBot using Scratch instructions
* What is an "Arduino board"
* What is the "Arduino Program" and how it corresponds to the "Scratch Program"
* How to upload a program to the mBot
* How to set the LEDs on the mBot to any colour

---

**This chapter contains hand-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will compose your first mBot sketch and learn how to upload it to your mBot.

---

You can now move on to compose your first mBot sketch.

Referring to Image 2.15.1, in the right bottom corner of the Scripts tab \(1\) you will find the "Robots" group of blocks \(2\). Once you select it, you will see the mBot blocks section \(3\) which contains all of the different programming blocks that you can use with the mBot.

![](/assets/Img.3.15.1.jpg)

\[Image 2.15.1: The mBot instruction blocks on the Scripts tab\]

Let's have a quick look at some of these instruction blocks.

The first one, for example, reads "run forward at speed 0". With this block you can make the mBot move forwards, backwards, left or right, at a particular speed.

Look at the other available blocks to become familiar with their names and shapes.

Find one that allows you to set the onboard LEDs to a specific colour.

Find another one that you can use for playing tones, or for detecting when the onboard button is pressed.

You will be using those blocks, and many more, later.

### Built-in and additional components

Out of the box, the mBot comes with a number of capabilities based on sensors or motors or other attachments like, for example:

* an ultrasonic sensor
* an infrared sensor
* a line follower module
* a light intensity sensor

As far as outputs and actuators are concerned, there are:

* two motors connected to two individual ports: one for each motor
* two RGB LEDs

Apart from these basic capabilities, though, you can purchase and plug onto the mBot additional components and eventually make use of the mBlock extension to interact with them. So, for example, you can purchase a sound sensor separately and use the corresponding mBlock instruction block to interact with it. A sound sensor is practically a microphone. You can program it so that when you clap your hands, for example, your mBot runs forward.

You can have a external 3-axis gyroscope, too, which is very good for detecting a change in direction like when the robot turns over, upside-down.

For this crash course on the mBot though, we will be focusing on the capabilities that the mBot comes with out of the box without any additional components.

### Creating a new program

Let's create a program now!

In order to create a new mBlock program you go to menu "File" and click on "New". In the "Scripts" tab, in "Robots", pick the "mBot Program" header block and drag and drop it into the scripts canvas. Every mBot program must start with this block.

Below it, you can attach other blocks that fit. For example, let's say that you would like to change the colour of the two onboard RGB LEDs. To do that, you pick the "set led on board..." instruction block and drag and drop it and connect it to the mBot header. Thereafter, you can configure it further by choosing which one of the two LEDs you would like to manipulate \(left/right/both\) and what colour to set by choosing values from 0 to 255 for all three red/green/blue attributes. Through the combination of these three, you can create all kinds of other composite colours. For our example let's just choose to turn on "all" LEDs and let's pick 255 for red and 0 \(zero\) for both green and blue. That should give a plain red colour to both the on-board LEDs.![](/assets/2017-04-12_10-06-37.png)

\[Image 2.15.2: A small program that will turn all LEDs to red\]

Once finished with the program, connect the USB cable to the USB port \(1\) on the mBot. You will know that the connection has taken place because there wil be a red LED \(2\) which indicates that the mBot is receiving power from the USB. But that's not enough power to power up the robot. Once you plug in the cable, turn on the mBot by moving the switch \(3\) to the "ON" position.Now, your mBot is ready to be programmed.

![](/assets/Img.3.15.3.jpg)

\[Image 2.15.3: Connecting the USB on the mBot\]

Next step is to go to the "Connect" menu and look for the serial port \(a COM port\) where the mBot is connected to the computer. It is always going to be a port that has a number larger than one. That is because COM1 is typically used by the operating system itself. In our example the port to which the mBot is connected happens to be COM4.

If you are using a Mac OS computer, the serial port will be something like `/dev/tty.wcyusbserial1410`. The numbers at the end of the serial port name may be different to what you see in this example.

![](/assets/Img.3.15.4.jpg)

\[Image 2.15.4: Connecting to the Serial Port\]

Next, you right-click on the mBot program and choose "Upload to Arduino".

![](/assets/upload to arduino.png)\[Image 2.15.5: Right click on the mBot Program block and click on "upload to arduino"\]

---

#### DID YOU KNOW?

Students often are confused about the "upload to arduino" option in the context menu. They think "What's the Arduino? I'm just trying to program my mBot!"

Remember, inside the mCore controller that sits on top of the mBot chassis is a custom version of an Arduino board. This is where your program is uploaded.

---

By doing that, you get to see the uploading component of the mBlock application. What you see there is the translation of the simple Scratch-based program in an Arduino program or "sketch" as we call it. You notice that we've got a lot of instructions there. Most of it is just the infrastructure for supporting the functionality that you have selected in the mBot program.![](/assets/Img.3.15.5.jpg)\[Image 2.15.6: The Scratch block corresponding to Arduino instructions\]

You want your mBot to just turn the two LEDs into red and the program shown above does just that: line 34 sets the colour to red and line 35 turns the LEDs on. Everything else that you see around is just in support of these two lines of instructions.

If you experiment further and drop some other block into the program, you will notice that another instruction is going to appear somewhere in the Arduino program. If you change the order of the instruction blocks, you are going to see that the Arduino instructions are going to change, accordingly.

---

#### TRY THIS NOW

Go ahead and drop a couple of blocks into the sketch area, while the Arduino pane is visible.

Notice how new text code is added when you drop a new block into the sketch area? Also try to do things like change the order or location, or parameters of these blocks and observe how the Arduino code is changing.

To delete a block, right click on it and click "Delete" from the context menu.

---

And that is how mBlock makes programming easy: it provides a graphical interface for the programmer where instruction blocks are just picked, dragged and dropped instead of typing traditional text-based instructions.

You can safely ignore the Arduino program and just click on the "Upload to Arduino" button that will transfer the program to the mBot.![](/assets/2017-04-12_10-32-35.png)\[Image 2.15.7: With the Arduino pane showing, click on the "Upload to Arduino" button to upload the program to your mBot\]

---

#### TROUBLESHOOTING

If the message "Please connect the serial port" appears, you just need to go to: menu Connect &gt; Serial Port and click on the right COM port. The message does not refer to a physical cable connection!

---

The upload process you now start. The process includes the compilation of your code. That means that the text Arduino program is being translated into binary \(a long string of zeros and ones\) which is the only programming format the Arduino can actually understand.

After the program uploads, you will see the two LEDs light up red.

Let's try a variation of the program now and have the right LED shine green and the left LED shine blue.

---

#### DID YOU KNOW?

You can just click on "Back", if you prefer to close the view of the Arduino program.

---

![](/assets/Img.3.15.6.jpg)\[Image 2.15.8: A program for setting two different colours. On the left in Scratch blocks, on the right in Arduino text.\]

Drag and drop blocks and change parameters until you have the program shown in the image above. Then right click on the program and "Upload to Arduino". You should be able to see, now, the mBot LEDs shining in accordance with the instructions: left one green, right one blue.

From here on, you can play some more and experiment with different colour value combinations. Remember that we are not confined to using the values from the drop-down. You can actually go and change that to any value between 0 and 255.

---

#### DID YOU KNOW?

To find the value for the Red, Green and Blue components of any colour, Google for "colour chooser" or "colour wheel"

---

### Questions

#### Question 3.15.1: Does the mCore include a light sensor?

A. Yes

B. No

_Answer: A_

---

#### Question 3.15.2: How does the mBot relate to the Arduino?

A. The Arduino is an additional component of the mBot

B. There is no relation.

C. The mBot's mCore controller is a custom version of the Arduino board.

D. It is the part of the screen where the text program appears.

_Answer: C_

---

#### Question 3.15.3: In what format is the program actually uploaded to the mBot?

A. The compiled \(binary\) version of the program is uploaded

B. The Arduino code version of the program is uploaded

C. The Scratch version of the program is uploaded.

D. No program is uploaded, the mBot is controlled by the computer.

_Answer: A_

---

#### Question 3.15.4: Fill in the RGB values of the colour known as “cornflower blue”. \(Hint: search on the internet for it\)

R = \_\_\_\_\_\_\_\_ G = \_\_\_\_\_\_\_\_ B = \_\_\_\_\_\_\_\_

_Answer: R = 100 G = 149 B = 237 - or search Google for "cornflower blue RGB values"_

---

**Checklist**

Double-check that at this point, the following are completed:

\[ \] You know how to start the composition of a program for the mBot

\[ \] You know how to reveal the Arduino code pane in mBlock

\[ \] You know how to upload a program to the mBot

\[ \] You understand the relation between a Scratch mBot program and the equivalent Arduino code.



