# Section 2

---

## Chapter 8: Demonstration of the mBlockly

---

**In this chapter you will learn about:**

* How to control the mBot using mBlockly on a tablet
* The various Scratch graphical blocks that are available and what they do
* How to assemble a simple Scratch program
* How to upload a Scratch program to the mBot

---

**This is a hand-on activity.**

You will not need any tools.

You will need your mBot and an iPad tablet computer with the mBlockly application installed.

![](/assets/2017-04-04_16-45-51.png)

Get mBlockly from the Apple App Store. Find a download link at learn.makeblock.com/en/software/

_At this time, mBlockly is not available for Android tablets._

---

In this chapter you will learn about mBlockly. Using mBlockly, you can create programs using the Scratch language and upload them to your mBot wirelessly. Your mBot will then function according to your program.

Immediately after starting the mBlockly on your tablet, it will detect a nearby mBot and you can tap on it, on the screen, to connect.

![](/assets/Mbot - 0080 - Ipad 2 - demo of Makeblock mblockly mblock.CONSTANT-00-07-25-736.png)

\[Image 8.1: Your tablet running mBlockly will detect your mBot very quickly\]

If it doesn't, check that your mBot is turned on, and that the Bluetooth module is in discovery mode. You can confirm that by looking for the blue, blinking LED of the Bluetooth module. If the blue LED is solid \(not blinking\) then you know that it is connected to another Bluetooth device. If this device is not your tablet, try turning the mBot off and then on again in order to switch the Bluetooth module back to discovery mode \(blinking blue LED\).

![](/assets/IMG_9727.JPG)

\[Image 8.2: Look at the blue LED of the Bluetooth module to determine the connection status\]

---

**Question 8.1: What is the purpose of the blue LED that you can see near the battery connectors on the mCore?**

A. It is the battery indicator

B. It is one of the programable RGB LEDs

C. It is the Bluetooth status indicator

D. It is the USB connection status indicator

_Answer: C_

---

**Question 8.2: You are trying to connect your mBot to your iPad, and you can see that the blue Bleutooth indicator LED is blinking. What does that mean?**

A. The mBot is not connected to a host

B. The mBot is connected to a host

C. The mBot is searching for a host

D. The mBot need a firmware upgrade

_Answer: A_

---

The programming happens using Scratch, which is a block-based programming language. There are a few few built-in programs, too, to get started. Let's start with a simple one.

![](/assets/Mbot - 0080 - Ipad 2 - demo of Makeblock mblockly mblock.CONSTANT-00-08-01-967.png)

\[Image 8.3: To load a program, tap on its thumbnail\]

---

**BEWARE!**

If the projects that you see in your Projects screen are not the ones that we show in Image 8.3, it's Ok! The mBlockly app is updated frequently, and these examples may change by the time you read this book. The purpose of this chapter is to make you familiar with the basics of using Scratch in mBlockly. If the sample projects in your mBlockly are not the same as the ones you see in Image 8.3, don't be discouraged. Simply tap on any of them and start exploring it on your own!

---

Tap on the one called: "run forward and backward" and have a look at the instruction blocks, which should be self-explanatory as they are phrased in natural language:

* run forward at speed 150; 
* wait for 2 seconds;
* run backward at speed 200 \(indefinitely, since there follows no other instruction to change this\). 

![](/assets/Mbot - 0080 - Ipad 2 - demo of Makeblock mblockly mblock.CONSTANT-00-08-17-385.png)

\[Image 8.4: To upload a program to the paired mBot, tap on "Go"\]

Click on "Go" to execute the instructions.

You can notice a little green glow around a block, as each of the instructions is executed by the mBlock. This helps follow step by step the execution of the program.

The problem with this program is that once your mBot starts to run backwards, it never stops. We should fix that!

Let's make an addition to the program: after the mBot runs backwards for two seconds, it should stop moving. To do that we need to introduce another two-second delay and then insert the "stop moving" block.

Here is how: Go to the "Control" submenu that you can find on the left side of the screen,  and use the "wait" block to insert a new two-second delay.

![](/assets/Mbot - 0080 - Ipad 2 - demo of Makeblock mblockly mblock.CONSTANT-00-09-35-387.png)

\[Image 8.5: To insert a block, select it from a submenu and drag it to your program. It will snap in place when you place it near a compatible block\]

Then, since you want to stop the motors, which is a movement type of instruction, go to the "Move" submenu, pick the "stop moving" block, drag it and place it right under the last two second wait.

![](/assets/Img.2.3.1.jpg)

\[Image 8.6: The program, with your modifications\]

Tap the "Go" button to see your mBot going forward for two seconds, then backwards for another two seconds and then  stop moving.

### The instruction groups

If you got it right, you can now start combining all the different types of blocks that are available in mBlockly. Check, for example, the instructions in the "Move" group by taping on the word "Move" from the menu on the left of the screen:

![](/assets/e596d7cc-5626-4aa5-a357-15ed5188276a.jpeg)

\[Image 8.7: The "Move" instructions\]

From top to bottom, you see instructions that will get the mBot to:

1. run forward at some speed and for a specific amount of seconds
2. rotate to some direction at some speed and for a specific amount of seconds
3. run forward at some speed without specifying the time to keep doing this
4. turn to some directions at a specific speed
5. stop moving
6. set a servo motor, located at some port and slot, to a specific degree

Next we have the instructions in the "Display" group:

![](/assets/91ce23c0-a970-4522-a251-07ee27a8b4ba.jpeg)

\[Image 8.8: The "Display" instructions\]

You can use these to:

1. set the colour of the LEDs to a specific colour
2. buzz a specific tone
3. stop a tone already sounding
4. change the colour of an RGB led module

A very useful feature are the "Events", which can be used to mainly detect movements of the tablet:

![](/assets/b1918a53-8366-4f28-b32d-e379a49f72c5.jpeg)

\[Image 8.9: The "Events" blocks\]

With the instructions in the Event group we can get the robot, for example, to move depending on whether the tablet is tilting forwards or backwards \(blocks 5 and 4\) using the tablet itself as a control device.

In the Detect group of instructions you can find blocks that work with sensors.

![](/assets/f787dcb0-1ab4-48c3-9761-1ed62863c304.jpeg)

\[Image 8.10: The "Detect" blocks\]

These can be used to take input from the sensors. Based on these readings, the mBot can decide how to move in the event of detecting an obstacle. For example, it can stop, turn left or right, or go around the obstacle.

In the Math submenu are blocks that can perform the basic mathematical and logical operations like addition, subtraction etc.:

![](/assets/a9bdda61-f991-41d1-a003-e3f1243ad05b.jpeg)

\[Image 8.11: The "Math" blocks\]

In the Control submenu are blocks that allow us to implement control structures.These structures allow your program to contain loops in which a segment of your program is executed repeatedly, or to execute part of your program depending on a condition.![](/assets/bf43ec4e-3e40-468e-8d2a-4cb2266ec148.jpeg)

\[Image 8.12: The "Control" structures\]

You can use these, for example, to repeat a set of instructions either forever or a particular number of times. Or even repeat until the sensor senses something, like an obstacle in front of it, for example.

Later on in the book we are going to explain the Scratch language and  how it implements to mBot. We will see more examples and explain how these blocks work as we are building the line-follower application. For now, you don’t need to worry much about the blocks although you will find that most of them are fairly self-explanatory.

### Experimenting with an existing project

Let’s try out some of the other projects. To do this, click on "My Projects" on the top right of your screen.

#### The Colour Show example

Tap on "Colour Show" and have a look at it. If this example is not available in the list of programs, that's OK. You can assemble it yourself by finding the right blocks inside the various submenus and connecting them together, as you can see in image 8.13.

---

**BEWARE!**

In Image 8.13 \(and in several other images\), the numbers inside the orange boxes are not part of the program! These are simply numbered pointers to different parts of the program so that we can reference them from this text.

---

![](/assets/88ea9406-0534-4aac-9872-765dcc62fce3.jpeg)

\[Image 8.13: The "Colour Show" program\]

In this example there is a loop block, called "repeat forever" \(block 1\). Anything you put inside this block will do exactly that, repeat for ever. In the repeat forever block, the first thing that happens is to turn both onboard RGB LEDs to red \(block 2\) and then to wait for a particular amount of time \(block 3\). The "wait" block requires a numerical value \(or variable and I’ll talk about variables in an upcoming chapter\). To provide a number, simply tap on the existing number of the "wait" block. This will bring up a keypad.

The problem here is that the keypad only allows whole numbers, known as integers, to be entered. If you need to introduce a smaller wait, say for 0.25 seconds, you can’t do it, since there’s no decimal point on the keypad. This is inconvenient, but there is a workaround.

We can click on the "Math" tab and take from there some mathematical function, like the division block in the program, and place it inside the wait block. Type "1" in the first numerical parameter of the arithmetic function block, select division for the function type, and type "5" for the second numerical parameter. This gives "0.25" for the wait time, which is what we want here.

---

**Remember**: If you need to delete a block, just drag and drop it in the dustbin that will appear on the left edge of the screen.

---

And this is what the program does: it sets the LEDs to red, then waits for 0.25 seconds, then sets the LEDs to green, again waits for 0.25 seconds, then sets the LEDs to blue, again waits for 0.25 seconds, and this process repeats itself over and over again.

To test it just tap on "Go" and you will be able to see the program run, one instruction after the other, and both the LEDs switching from one colour to the other, waiting in between one quarter of a second every time.

### Where the program executes

When you write a program using mBlockly, you should remember that the program is actually running on the tablet, not on the mBot. On the mBot itself, and inside the microcontroller, a remote control program is executed, basically waiting for instructions from the tablet, transmitted via Bluetooth. The mBot is just connected and remotely controlled by the tablet.

That has a detrimental effect on the speed by which the instructions get executed: the execution speed is actually very low. There are many types of applications that you will not be able to implement on your mBot by remote control, like the line-follower ones. The problem here is that the speed by which the mBot needs to take readings of its line-following module and from the distance sensor, and then translate that information into a movement for the motors, has to happen very quickly and the slow pace of the tablet execution will just not do.

Just remember that the applications shown here are good for a few simple types of programming with the mBot but you will grow out of them fairly quickly. For more sophisticated programs we will need to move to the computer. A significant part of this course is dedicated to programming the mBot on the computer in order to maximize the efficiency of the mounting tool on the mBot.

---

**Question 8.1: What is the way to insert decimal numbers \(i.e. numbers like 0.5, 1.0 or 5.25\) in a wait block?**

A. Use the decimal point in the keypad to type in the number

B. Use an arithmetic function block to calculate the decimal number from two integers

C. It is not possible to insert decimal numbers in a wait block. A wait block will only accept integer numbers.

_Answer: B_

**Question 8.2: Where is the Scratch program that you write in mBlockly executed?**

A. On the mCore microcontroller

B. On the tablet. The mBot is controlled remotely by the program running on the tablet.

_Answer: B_

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] You have installed mBlocky on your iPad

\[   \] You have successfully connected your mBot to your iPad

\[   \] You have successfully uploaded a program that you wrote in mBlockly on your iPad to your mBot

\[   \] You are familiar with the basic Scratch blocks in mBlockly

---



