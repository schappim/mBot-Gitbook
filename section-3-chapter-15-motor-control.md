# Section 3

---

## Chapter 14: Motor control

---

In this chapter you will learn:

* 1

---

In the last chapter we learned how to get the two LEDs to display two different colors. In this part of the crash course, we are going to learn how to use the two motors. Each mBot comes with two motors, left and right, depending on how you look at it.

They are connected each one to one of two ports like shown in the image below.

![](/assets/Img.3.16.1.jpg)

\[Image 2.16.1: The two motor connectors\]

Let's create a new program in order to see how to use the motors. Again, to do this, we go to the "File" menu and then click on "New".

Now, just like in the previous example, we'll start by dragging and dropping instruction blocks onto the canvas, the first one being the "mBot program" block.

There are couple of blocks that allow us to control the motors. Let's start with block "run forward at speed 0" which allows us to get the mBot to move forwards or backwards and turn left or right. We pick it and attach it to the "mBot program" header block and then we can configure its two attributes:

a. the direction of the move

b. the speed

The speed can take any number between -255 and 255. Again, instead of selecting one of the values from the drop-down, you can click and enter any valid value. A negative value here will have the robot run backwards, if configured to run forward, and vice versa. Let's choose "forward" and a speed of 125.

**Note**: The speed number is rather arbitrary and how fast the robot goes really depends on how depleted are the batteries or whether there is some heavy load on the robot.

Let's add now a wait block and set it to 5 seconds and another "run forward ..." and set it at a speed zero, which should stop the spinning of the wheels.

![](/assets/Img.3.16.2.jpg)

\[Image 2.16.2: The described Scratch code and the corresponding Arduino code\]

We right click, now, on the program and upload it. We should first make sure, thought, that we are connected to the appropriate COM port, like we saw in the previous chapter.

We might want to hold the mBot up because it is going to start running the sketch immediately and the wheels are going to start spinning.

 zero because zero means that the motors have stopped spinning. Let's upload again to the Arduino. You can see that the sketch has been updated with the new command. Here's my delay five. Here's the move and the speed here is zero. Upload it. Uploading, writing, reading there you go, and stopped.

There was -- I think you can get about five seconds and the wheels then stopped after five seconds because it reached the last around forward statement which was asking -- which was instructing the robot to stop from moving. Now, what I'll do is I would like to test my robot on the floor so I can actually see it moving. To do that, I simply remove the USB cable. Since I've got the battery connected the **\[unintelligible 00:07:54\]** is still powered and I'm going to turn it off. Now, when it turn it back on, the program is always stored inside the Arduino that runs the mBot and execute automatically. It will execute one time and then it will stop. If I want to re-execute the program, I've got to power cycle the mBot. I've got to turn it off and then back on.

Another way to get your mBot to execute the program again is to reset it. There is a reset button right here, right inside this little hole. You need to use a tool to be able to reach there. I'm going to use my tweezers. Use the tweezers and set it inside the little opening of the case. Press the button and then the program will executes again. That's a alternate way of running a resident sketch instead of power cycle.

The reset button is the same as this reset button on the Arduino board. The effect is exactly the same. It will re-execute the program that is stored on the chip on the out maker. Let's take my mBot over to the floor where I've already set the track that eventually the mBot will be following to see it moving forwards for five seconds and then stopping. I will turn off the mBot and then turn it back on, and off it goes. Five seconds later, it stops. Awesome. The mBot has performed as expected. Now, the next thing that I'd like to do is to get the mBot to turn left, right and then move backwards as well.

