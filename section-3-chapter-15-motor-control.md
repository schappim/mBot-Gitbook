# Section 3

---

## Chapter 16: Motor control

---

In this chapter you will learn about:

* How to program the mBot to move forwards
* What is the meaning of the speed values
* How to re-execute a program

---

In the last chapter we learned how to get the two LEDs to display two different colours. In this part of the crash course, we are going to learn how to use the two motors. Each mBot comes with two motors, left and right, depending on how you look at it.

They are connected each one to one of two ports like shown in the image below.

![](/assets/Img.3.16.1.jpg)

\[Image 2.16.1: The two motor connectors\]

Let's create a new program in order to see how to use the motors. Again, to do this, we go to the "File" menu and then click on "New".

Now, just like in the previous example, we'll start by dragging and dropping instruction blocks onto the canvas, the first one being the "mBot program" block.

There are couple of blocks that allow us to control the motors. Let's start with block "run forward at speed 0" which allows us to get the mBot to move forwards or backwards and turn left or right. We pick it and attach it to the "mBot program" header block and then we can configure its two attributes:

a. the direction of the move

b. the speed

The speed can take any number between -255 and 255. Again, instead of selecting one of the values from the drop-down, you can click and enter any valid value. A negative value here will have the robot run backwards, if configured to run forwards, and vice versa. Let's choose "forward" and a speed of 125.

**Note**: The speed number is rather arbitrary and how fast the robot goes really depends on how depleted are the batteries or whether there is some heavy load on the robot.

Let's add now a wait block and set it to 5 seconds and another "run forward ..." and set it at a speed zero, which should stop the spinning of the wheels.

![](/assets/Img.3.16.2.jpg)

\[Image 2.16.2: The described Scratch blocks and the corresponding Arduino text\]

We right click, now, on the program and upload it. We should first make sure, of course, that we are connected to the appropriate COM port, like we saw in the previous chapter. We might also want to hold the mBot up because it is going to start running the sketch immediately and the wheels are going to start spinning.

After uploading the program we should see the wheels spinning for 5 seconds and then stop.

In order to test the robot on the floor we should turn the switch off, unplug the USB cable and put it the robot on some clear space.

The mBot is powered by the batteries and the program is always stored inside the Arduino board. Turning the mBot back on will execute it automatically, but then only once.

There are two ways to re-execute the program:

1. by powering cycle the mBot: turning it off and then back on.
2. by pressing the reset button on the mBot

The reset button does exactly that: it executes the program stored on the chip, on the Arduino board.

In the next chapter we are going to see how to get the mBot to turn left, right and then move backwards, as well.

### Questions

1.What will be the effect of this command: "run backward at speed -100"

**A. It will have the mBot move forwards**

B. It will have the mBot move backwards

C. It will have the mBot to stop

D. It will return an error

2.How can we re-execute the program?

A. By creating a new program

B. By clicking on the reset button, on the mBot

C. By turning off the mBot, and then back on

**D. Both B and C**

