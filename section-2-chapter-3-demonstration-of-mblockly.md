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

\[Image 2.3.6: The "Control" structures\]

We can use these, for example, to repeat a set of instructions either forever or at a particular number of times. Or even repeat until the sensor senses something, like an obstacle in front of it, for example.

Later on in the book we are going to explain the Scratch language and handle how it implements to mBot. We will see more examples and explain how these blocks work as we are building the line follower application. For now, you don’t need to worry much about the blocks although you will find that most of them are fairly self-explanatory.

~~**{up to here by Dimitris}**~~

Let’s go back to some of my other projects and I’d like to give you one more example. Let’s have a look at this Colour Show. Tap on Colour Show to bring it up and you can see that I’ve got a loop, repeats forever and you can probably guess what this does. What I’ve got in this example here is a loop, first of all, that never ends, so it repeats forever. The first thing that happens in the loop is to first turn both onboard RGB LEDs to red and then to wait for a particular amount of time.

I just want to show you something. The wait block requires a numerical or a variable, and I’ll talk about variables in oncoming lecture. But the problem here is that the keypad that I used or that is provided to input a number only gives me the ability to type in whole numbers, whole integers. If I want to introduce a wait for say 0.25 seconds, then I can’t do that here because there’s no decimal point. That’s pretty bad but there is a workaround on that.

What I can do is to insert a mathematical function like this one, to replace the integer and then in that mathematical function, I won’t try it again. \[laughs\] Then take that function, take that arithmetic calculation and put it inside my wait block. I need one more number block, so I put that in there. Now I can just do a division between this case one divided by five, and that will give me a result that is less than one. In that way, I can have a wait period, same set it into my program that are less than one second or at least that include a decimal.

If you want to delete a block, just tap it and move it on to the left, and it will disappear. After I wait for 0.25 seconds, while both LEDs on board are red, then switch to green, wait for the same amount of time, then switch to blue, wait for the same amount of time and then go back and start with the red again. Let’s upload that program and you can see how the LEDs -- I can’t get a better view like that. The LEDs rotate between red, green and blue.

Okay. Now, the other thing to remember is with all these applications, the program is actually running on my iPad. On the mBot itself, inside the microcontroller on the mBot, I’m executing a remote control program. That program basically is waiting for instructions from the iPad transmitted to it via Bluetooth and just turning on its LED. Taking a reading of the sensor or moving its motors or activating its motors. But none of the processing is happening on the mBot itself. The mBot is just connected and remotely controlled by my iPad.

Then has a detrimental effect on the speed by which it can execute those instructions. The speed is actually very, very low. There’s a whole bunch of applications that you will not be able to implement on your mBot by remote control. One of those applications sees the line follower applications, because the speed by which the mBot needs to take readings of its line followings sensors down here and from the ultrasonic sensor and then translate that information into a movement for the motors. That has to happen very, very quickly. It’s just not enough time for the iPad to do the processing and send the instructions to the mBot for it to execute them on time.

Just remember that the applications that I'm showing you here on the tablet are good for a few simple types of programming with the mBot but you will grow out of them fairly quickly if you want to do something more sophisticated, and then we'll have to move unto the computer to do a program that is more efficient. I'm going to show you that later as well. Actually, I've got the bulk of this course dedicated to programming the mBot on the computer in order to maximize the efficiency of the mounting tool on the mBot.

Before that, I’m going to stop the execution of the program and show you the last example.

