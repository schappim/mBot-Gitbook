# Section 5

---

## Chapter 26: The line sensor

---

In this chapter you will learn about:

* How the line-follower sensor works
* How to use the line-follower block
* How to program the LEDs to shine according to the line follower status

---

We have covered a lot of details in the previous chapters, but the fun is actually starting now. We are going to play around with the line-follower module which is attached to the bottom of the mBot and even though it behaves as one single unit, it actually contains two sensors, as can be seen in the image below. These two sensors can detect light intensity \(darkness or lightness\) of a colour right in front of them.

![](/assets/Img.5.26.1.jpg)

\[Image 5.26.1: The two light intensity sensors on the line-follower module\]

First things first, we should make a line on the floor, using the line segments provided in this book.

Now let's make a little experiment: let's place the mBot on that dark line and move it a little to the left or to the right so that one of the light intensity sensors is above the line, and the other is not. We will notice that there are two tiny indicator LEDs on the module, each one corresponding to one of the sensors. Each of these LEDs is automatically turned on, when the corresponding sensor senses brightness underneath, like the white paper, and turned off when there is darkness, like the black line.

We can test this by moving the sensor to the left and to the right, relatively to the line.

If both of the sensors happen to be over the white part of the paper, outside the black line, both their LEDs will be turned on. If they are both over the black line, their LEDs will be turned off.

Programmatically, there is a "line follower \[Port\]" block available that returns the status of the line-follower module in the form of a number, ranging from 0 to 3, with one of the following meanings:

0 = both sensors sense darkness \(they see the black line\) and both indicator LEDs are off.

1 = left sensor senses darkness \(the line\), right sensor senses brightness \(the white paper\); left LED is off, right LED is on.

2 = left sensor senses brightness \(the white paper\), right sensor senses darkness \(the line\); left LED is on, right LED is off.

3 = both sensors sense brightness \(they see the white paper\) and both indicator LEDs are on.

![](/assets/Img.5.26.2.jpg)

\[Image 5.26.2: The "line follower \[Port\]" block\]

Notice that the attribute, in the image above, indicates that the line-follower module is connected on Port 2 of the mBot. If we need to connect it to a different port we should change this attribute accordingly.

We can use this block to read the value that the sensor sends back to the Arduino, inside the mBot, and determine what it is that the sensor is looking at: whether it is still completely inside the line, completely outside the line, or if one of the two sensors is inside the line and the other one outside it. Depending on this reading, we can decide whether the mBot needs to turn a little either to the left or the right, so that both sensors get to see the line again.

Let's get started with a little demonstration now.

Before actually implementing the line-following capability, involving the motors, let's just get the status information from the sensors and use it to turn the LEDs on and off, accordingly. In other words, let's copy the state from each one of the two indicator LEDs, on the line-follower module, to the two bigger LEDs of the mBot.

Let's create a new project therefore: File &gt; New and following, let's create the program shown below:

![](/assets/Img.5.26.3.jpg)

\[Image 5.26.3: The program that copies the status of the sensors to the LEDs of the mBot\]

First of all, notice that we have created a variable named "line\_sensor\_status".

Here's what happens in this program:

First we get the reading of the line follower and assign it to variable "line\_sensor\_status". Then we check the value of this variable, which is actually the sensor reading. As we said earlier it can be either 0, 1, 2 or 3. We choose to turn on the mBot LEDs according to this value: If it is 0, we know that both sensors are on the black line, so we turn both LEDs off. Else, if it is 1, we know that the right sensor sees the white paper, so we turn the right LED on. Else, if it is 2, we know that the left sensor sees the white paper, so we turn the left LED on. Else, it has to be 3, meaning that both sensors see the white paper, and we turn both LEDs on. And that, over and over again, getting each time a new reading, and having the LEDs shine accordingly.

Let's "Upload to Arduino" now, and check the program. We place the line follower module of the mBot on the line and experiment with it: move it a little to the left, a little to the right, so that the sensors get on and off the black line, and we should notice that the LEDs are turned on and off accordingly, indicating what it is that the two sensors see: the black line or the white paper.

And since we have done all this interesting work, let's don't forget to save the program: File &gt; Save Project as and give it the name "Line sensor with LEDs".

In the next chapter, we will get the motors to move the robot forwards and if the sensor detects that it is about to get outside of the line, get the robot to do a small correction towards the appropriate direction, and then move forwards, test again and constantly correct its course by adjusting the speed of the motors.

### Questions

Question 5.26.1: How many different statuses does the line follower have?

A. None

B. Three

C. Four

D. It depends on the port, where the sensor is connected.

_Answer: C_

Question 5.26.2: What does the "line-follower" block actually do?

A. It evaluates to either true or false, depending on the line follower reading.

B. It returns the status of the line -follower module.

C. It returns the number of the port where the line follower is connected.

D. It sends directions to the line-follower.

_Answer: B_

