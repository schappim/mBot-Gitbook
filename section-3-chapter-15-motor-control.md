# Section 3

---

## Chapter 16: Motor control

---

In this chapter you will learn about:

* How to program the mBot to move forwards
* What is the meaning of the speed values
* How to re-execute a program

---

**This chapter contains hand-on activities.**

You will not need any tools.

You will need mBlock installed on your computer. In this chapter you will only compose programs that control the Panda Sprite in the Stage area. You will not need your mBot, so you may put it aside for now

---

In the last chapter you learned how to get the two LEDs to display two different colours. In this part of the crash course, you are going to learn how to use the two motors. Each mBot comes with two motors, left and right, depending on how we look at it.

They are connected to one of two ports as shown in the image below.

![](/assets/Img.3.16.1.jpg)

\[Image 2.16.1: The two motor connectors\]

Let's create a new program in order to see how to use the motors. Again, to do this, you should go to menu "File" and click on "New".

Now, just like in the previous example, you can start by dragging and dropping instruction blocks onto the canvas, the first one being the "mBot program" header block.

There are a couple of blocks that allow you to control the motors. Let's start with block "\[run forward\] at speed \[0\]" which allows us to get the mBot to move forwards or backwards and turn left or right. Pick it and attach it to the "mBot program" header block and then continue by configuring its two attributes:

a. the direction of the move

b. the speed

The speed can take any number between -255 and 255. Again, instead of selecting one of the values from the drop-down, you can click and enter any valid value. A negative value here will have the robot run backwards \(with the direction attribute set to "run forward\]\) and vice versa. Let's choose "forward" and a speed of 125.

**Note**: The speed number is rather arbitrary and how fast the robot goes really depends on how depleted are the batteries or whether there is some load on the robot.

Let's add now a wait block and set it to 5 seconds and another "run forward ..." and set it at a speed zero, which should stop the spinning of the wheels.

![](/assets/Img.3.16.2.jpg)

\[Image 2.16.2: The described Scratch blocks and the corresponding Arduino text\]

Right click, now, on the program and upload it. You should make sure first, of course, that you the mBot is connected to the appropriate COM port, like we saw in the previous chapter. You might also want to hold the mBot up because it is going to run the sketch immediately and the wheels are going to start spinning.

After uploading the program you should see the wheels spinning for 5 seconds and then stop.

In order to test the robot on the floor you should turn the switch off, unplug the USB cable and put the robot on some clear space.

The mBot is powered by the batteries and the program is always stored inside the Arduino board. Turning the mBot back on will execute it automatically, but then only once.

There are two ways to re-execute the program:

1. by powering cycle the mBot: turning it off and then back on.
2. by pressing the reset button on the mBot

**Note**: The reset button does exactly that: it executes the program stored on the chip, on the Arduino board.

In the next chapter we are going to see how to get the mBot to turn left, right and then move backwards, as well.

### Questions

Question 3.16.1: What will be the effect of this command: "run backward at speed -100"

A. It will have the mBot move forwards

B. It will have the mBot move backwards

C. It will have the mBot stop

D. It will return an error

_Answer: A_

Question 3.16.2: How can we re-execute the program?

A. By creating a new program

B. By clicking on the reset button, on the mBot

C. By turning off the mBot, and then back on

D. Both B and C

_Answer: D_

