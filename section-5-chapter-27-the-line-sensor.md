# Section 5

---

## Chapter 26: The line sensor

---

In this chapter you will learn about:

* Ho
* How

---

We had to covere a lot of details in the previous chapters, but the fun is actually starting now. We are going to play around with the line-follower sensor. This is a module that attached at the bottom of the mBot and even though it behaves as one single unit, it contains two sensors, like can be seen in the image below, which detect light intensity \(darkness or lightness\) of a color right in front of them.

![](/assets/Img.5.26.1.jpg)

\[Image 5.26.1: The two light intensity sensors on the line-follower module\]

First things first, we should make a line on the floor, using the line segments provided in this book.

Now let's make a little experiment: let's place the mBot on that dark line and move it a little to the left or to the right so that one of the light intensity sensors is above the line, and the other is not. We will notice that there are two tiny indicator LEDs on the module, each one corresponding to one of the sensors. Each of these LEDs is automatically turned on, when the corresponding sensor senses brightness underneath, like the white paper, and turned off when there is darkness, like the black line.

We can test this by moving the sensor to the left and to the right, relatively to the line.

If both of the sensors happen to be over the white part of the paper, outside the black line, both their LEDs will be turned on. If they are both over the black line, their LEDs will be turned off.

Programmatically, there is a "line follower ..." block available that returns the status of the line-follower module in the form of a number, ranging from 0 to 3, as follows:

0 = both sensors sense darkness \(they see the black line\) and both indicator LEDs are off.

1 = left sensor senses darkness \(the line\), right sensor senses brightness \(the white paper\); left LED is off, right LED is on.

2 = left sensor senses brightness \(the white paper\), right sensor senses darkness \(the line\); left LED is on, right LED is off.

3 = both sensors sense brightness \(they see the white paper\) and both indicator LEDs are on.

![](/assets/Img.5.26.2.jpg)

\[Image 5.26.2: The "line follower ..." block\]

Notice that our line-follower module is connected on Port 2, of the mBot. If we need to connect it to a different port we should change the attribute of the line follower accordingly.

We can use this block in order to read the values that the sensor sends back to the Arduino, inside the mBot, and determine what is it that the sensor is looking at. Whether it is still completely inside the line, completely outside the line, or if one of the two sensors is inside the line and the other one outside it. Depending on this reading, we can decide whether the mBot needs to turn a little either to the left or the right, so that both sensors get to see the line, again.

Let's get started with a little demonstration, now.

Before actually implementing the line-following capability, involving the motors, let's just get the status information from the sensors and use it to turn the LEDs on and off, accordingly. In other words, let's copy the state from each one of the two indicator LEDs, on the line-follower module, to the two bigger LEDs of the mBot.

Let's create a new project therefore: File &gt; New

Following, let's create the program shown in the below:

![](/assets/Img.5.26.2.jpg)

\[Image 5.26.3: The program that copies the status of the sensors to the LEDs of the mBot\]

First of all, notice that we have created a variable named "line\_sensor\_status".

Here's what happens here:





sensors in the line following sensor and to replicate the status on the on board LED. If the sensor is fully within the black line, and I would like the two LEDs to be turned off. If the sensor is fully outside the black line, then I would like both LEDs to be turned on. If the sensor is partially inside or partially outside the line, it sent depending on how you see these things.

Then, I would like to have, say in this case, the left LED turned on, while the right one turn these, turned off and vice versa. If it's in this state, then I'd like this LED to be off and that to be on. Let's start writing that little sketch. As always, I'll start with the mBot program head on because I want the reading of a sensor to happen continuously. I will be using the forever loop. Now the line follower go back to the robots, and you can see that there is a block that allows us to read the line-following sensor. Here it is, the line following sensor. There is another line follower block, this one here, that allows us to read the individual light sensors on the line sensor.

You can read either the left or the right side of the line sensor, but we're not going to use that in this example. You can experiment with this, of course. Now the line follower, can be connected to any one of the ports. Right now, I have it connected to port number two. I've got the port number two set for this line follower block. Now you can see that this is a block with rounded ends. If you remember, that means that this block returns a number and that we need to capture this number inside a variable. Let's go to data and blocks and create this variable. Let's call it Line Sensor Status or you can choose your own name. Let's set this variable with whatever the line follower block returns.

This is what we want to do at the beginning of every forever loop, is to take a reading from the sensor, and use that reading and store it inside the line sensor status variable. Then depending on what the line follower returns the value that we store in the line sensor status, we want to turn on the appropriate LED. The line follower block returns a number and that number depends on the condition of each one of the two sensors. We've got one sensor here, and one sensor here. This is sensor number one, and this is sensor number two. If the robot is positioned like this, with sensor number one being outside the black line, then line follower returns returns a value two.

If the robot is positioned like this, where sensor number two is outside the black line, then the sensor and the line follower block returns a value of one. If both sensors are inside the black line, then the block returns a value of zero. Zero means that both sensors one and two are inside the black line. Let's take advantage of this. We're going to use, again, the if-else block, going to put it straight inside the forever loop, and then I'll use one of the operators. The first operator to try out is this. I'm going to use the equal operator because what I want to say is that if line sensor is zero, it means that both sensor number one and sensor number two are inside a black line.

Let's go grab the LED onboard block, and I wouldn't turn both of them off. If that is not true, then three other things may be happening. The sensor is either at this position, halfway in the black line or this position, also halfway in the black line or it's completely outside the line. Let's implement the first two conditions. Again, we're going to look at an if-else-then control structure and the first condition that I'd like to implement is that of, let's say you're going to get an operator.

I'm going to use the equal separator because I want to test that the line sensor status is one. If the line sensor status is one, then you can take another on board LED and one means that a robot is at this position here. The first sensor is on the black line, the second sensor is outside the black line. When that happens, I would like to turn the right LED on. I'll just use a green component. Now if the status is not zero and is not one, then there could be two values that the sensor could be. I have to go back to into control and grab another if else if I've got another two values to test and the first value be again equal. Now, I'm going to test for the line sensor status being two which represents this position of the robot over the line.

When that is through, what I'd like to do is to turn the left LED on. Can still be green. There's one condition left to do. If none of the above is true, then we're going to end up in this last area of the last, if else block. When that happens, what I'd like to do is to turn both LEDs on, make them both green. Let's see if this actually works by uploading a program to the Arduino. Upload. Program uploaded. Let's see that actually works as expected. We've got the sensor number one, that is outside the black line sensor. Number two is on the black line.

The LED for sensor number is eliminated indicating this and that corresponds to the green LED on the mBot board copying that state. I'm going to move the sensor fully within the line, and you can see now that all LEDs are off. Then move it half outside on the other side of the line. Green LED goes on the correct side and finally, fully outside the black line and both equal LEDs are on. That works. I'm going to save this little program when you're ready to move on to the next step.

In the next step, what we'll do is engage the motors. We're going to get the motors to move the robot forwards, and if the sensor detects that it's about to get outside of the line, to get the robot to do a small correction towards the appropriate direction, and then move forwards again and test again. Then constantly corrects its course by adjusting the speed of the motors. We'll do that next.

