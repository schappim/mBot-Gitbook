# Section 2

---

## Chapter 3: Demonstration of the mBlockly

---

In this chapter you will learn about:

* How to control the mBot using mBlockly on a tablet

---

In this chapter we are going to see what mBlockly is like.

Immediately after starting the app on your tablet, mBlockly will detect a nearby mBot and you can tap on it, on the screen, to connect.

The programming happens using Scratch, which is a block-based programming language. There are a few few built-in programs, too, to get started. Let's start with a simple one. Tap on the one called: "run forward and backward" and have a look at the code blocks which should be self explanatory as they are phrased in natural language:  run forward at speed 150; wait \(actually continue doing that\) for 2 seconds and then run backward at speed 200 \(indefinitely, since there follows no other instruction to change this\). Click on "Go" to execute the instructions.

You can notice a little green highlight, moving from one instruction being executed to the next. This helps follow step by step the execution of the program.

Let's try to make an addition to the code: after the mBot runs backwards for two seconds, it should stop any movement completely. To do that we need to introduce another two-second delay and here is how: Go to "Control" and use the wait component to insert a two-second delay. Then remember I want to stop the motors, which is a movement type of instruction. So go to "Move", pick the "stop moving" block, drag it and place it right under the last two second wait.

![](/assets/Img.2.3.1.jpg)

\[Image 2.3.1: Code\]

Hit the "Go" button to see the mBot going forward for two seconds, then backwards for another two seconds and then  stop moving.

### The instruction groups

If you got it right, you can actually start combining all the different types of blocks that are available in this app. Check, for example, the "Move" instructions:

![](/assets/Img.2.3.2.jpg)

\[Image 2.3.2: The "Move" instructions\]

From top to bottom, you see instructions that will get the mBot to:

* run forward at some speed and for a specific amount of seconds
* rotate to some direction at some speed and for a specific amount of seconds
* run forward ad some speed without specifying the time to keep doing this
* turn to some directions at a specific speed
* stop moving
* set a servo motor, located at some port and slot, to a specific degree

Now proceed to the Display instructions:

![](/assets/Img.2.3.3.jpg)

\[Image 2.3.3: The "Display" instructions\]

You can use these to:

* set the colour of the LEDs to a specific colour
* to buzz a specific tone
* to stop a tone already sounding
* ~~**\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#???**~~

A very useful feature are the "Events" which can be used to mainly detect movements of the tablet:

![](/assets/Img.2.3.4.jpg)

\[Image 2.3.4: The "Events"\]

With these event blocks we can get the robot, for example, to move depending on whether the tablet is tilting forwards or backwards using this way the table itself as a control device.

![](/assets/Img.2.3.5.jpg)

\[Image 2.3.5: The "Detect" instructions\]

These can be used to take input from the sensors. Thereafter we can take descisions based on these readings and if there’s an obstacle detected, for example, we can get the mBot to stop moving.

There are instruction blocks that can perform the basic mathematical and logical operations like adding, subtracting etc.:

![](/assets/Img.2.3.6.jpg)

\[Image 2.3.6: The "Math" instructions\]

And then we can implement the basic programmatic control structures like making choices and executing loops:

![](/assets/Img.2.3.7.jpg)

\[Image 2.3.7: The "Control" structures\]

We can use these, for example, to repeat a set of instructions either forever or at a particular number of times. Or even repeat until the sensor senses something, like an obstacle in front of it, for example.

Later on in the book we are going to explain the Scratch language and handle how it implements to mBot. We will see more examples and explain how these blocks work as we are building the line follower application. For now, you don’t need to worry much about the blocks although you will find that most of them are fairly self-explanatory.

### Experementing with ready projects

Let’s go back now and try out some of the other projects. To do this, click on "My Projects" on the top right of your screen.

#### Colour Show

Let's tap on "Colour Show" and have a look at it.

![](/assets/Img.2.3.8.jpg)

\[Image 2.3.8: The "Colour Show" code\]

In the example we have got a loop that repeats forever and you can probably guess what this does.The first thing that happens in this loop is to turn both onboard RGB LEDs to red and then to wait for a particular amount of time. Now, the wait block requires a numerical value \(or variable and we I’ll talk about variables in oncoming chapter\). The problem here is that the keypad provided there to input a number only allows whole numbers, known as integers. If you need to introduce a wait for say 0.25 seconds, you can’t do it, since there’s no decimal point on the keypad, which is pretty bad but there is a workaround.

We can click on the "Math" tab and take from there some mathematical function, like the one in the code, and place it inside the wait block. One divided by five will give 0.25 and this is the way to wait for periods that include a decimal.

**Remember**: If you need to delete a block, just drag and drop it in the dustbin that will appear on the left.

And this is what the code does: it sets the LEDs to red, then waits for 0.25'', then sets the LEDs to green, again waits for 0.25'', then sets the LEDs to blue, again waits for 0.25'', and this procedure repeats itself over and over again.

To test it just click on "Go" and you will able to see the program run, one instruction after the other, and both the LEDs switching from one colour to the other, waiting in between one quarter of a second, every time.



With all these applications, the program is actually running on the tablet. On the mBot itself, and inside the microcontroller, a remote control program is executed, basically waiting for instructions from the tablet, transmitted via Bluetooth. The mBot is just connected and remotely controlled by the tablet.

That has a detrimental effect on the speed by which the instructions get executed: the speed is actually very, very low. There’s a whole bunch of applications that you will not be able to implement on your mBot by remote control like the line follower ones. The problem here is that the speed by which the mBot needs to take readings of its line following sensors and from the ultrasonic sensor and then translate that information into a movement for the motors, has to happen very quickly and the slow pace of the tablet execution will just not do.

Just remember that the applications that I'm showing you here on the tablet are good for a few simple types of programming with the mBot but you will grow out of them fairly quickly if you want to do something more sophisticated, and then we'll have to move unto the computer to do a program that is more efficient. I'm going to show you that later as well. Actually, I've got the bulk of this course dedicated to programming the mBot on the computer in order to maximize the efficiency of the mounting tool on the mBot.

Before that, I’m going to stop the execution of the program and show you the last example.

