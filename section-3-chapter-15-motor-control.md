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

The speed can take any number between -255 and 255. Again, instead of selecting one of the values from the drop-down, you can click and enter any number between A negative value here will have the robot run backward, if configured to run forward, and vice versa.

**Note**: The speed number is rather arbitrary and how fast the robot goes really depends on how depleted are the batteries or whether there is some heavy load on the robot.



 -255 and 255.



 You can go for anything else in between those values. So we can go for, say, 125. Let's see what the effect of this is. I've got my upload to the Arduino programming side of the M block application already displaying. You can see that as I dropped the movement block onto the canvas here, then the setup method of the Arduino sketch updated itself with the value that I prescribed, with the value that I typed in, 125 and 125 here on the block.

Let's upload that. First, I'll make sure that I'm connected to the appropriate com port. You can see that before the break, I had com four, now it's com six. It's because I turned off and then back on the mBot and that assigned it automatically to a new port. It doesn't really matter. I just reconnect to com six, done, and upload to the Arduino which means upload to the mBot. I'm going to hold it up a little bit because this is going to start running the sketch immediately. The wheels are going to start spinning. If I leave it on the table, it's just going to run off the table and fall on the floor. Writing, reading, there you go.

When I work with the mBot on my table, I often just turn it upside down so that I don't have to chase the mBot around my table. Now, this is going to continue spinning indefinitely because I haven't configured my program to do something like stop the wheels from spinning after a particular number of seconds. It's just going to go on indefinitely.

How about we get the robot to move forwards at this particular speed for five seconds and then I'd like it to stop. How do we do that? You may remember from the experimentation we did earlier with the sprite, that there is a function called wait. Go back to the control section of the scripts tab and there's a wait block here. I'm going to drag that and put it after my run block. I configured this to operate for five seconds. I'm going to include a wait block here that waits at this location of the program for five seconds .

Now, go back to robots, pick the run forwarded speed block again. But this time I'm going to leave it at zero because zero means that the motors have stopped spinning. Let's upload again to the Arduino. You can see that the sketch has been updated with the new command. Here's my delay five. Here's the move and the speed here is zero. Upload it. Uploading, writing, reading there you go, and stopped.

There was -- I think you can get about five seconds and the wheels then stopped after five seconds because it reached the last around forward statement which was asking -- which was instructing the robot to stop from moving. Now, what I'll do is I would like to test my robot on the floor so I can actually see it moving. To do that, I simply remove the USB cable. Since I've got the battery connected the **\[unintelligible 00:07:54\]** is still powered and I'm going to turn it off. Now, when it turn it back on, the program is always stored inside the Arduino that runs the mBot and execute automatically. It will execute one time and then it will stop. If I want to re-execute the program, I've got to power cycle the mBot. I've got to turn it off and then back on.

Another way to get your mBot to execute the program again is to reset it. There is a reset button right here, right inside this little hole. You need to use a tool to be able to reach there. I'm going to use my tweezers. Use the tweezers and set it inside the little opening of the case. Press the button and then the program will executes again. That's a alternate way of running a resident sketch instead of power cycle.

The reset button is the same as this reset button on the Arduino board. The effect is exactly the same. It will re-execute the program that is stored on the chip on the out maker. Let's take my mBot over to the floor where I've already set the track that eventually the mBot will be following to see it moving forwards for five seconds and then stopping. I will turn off the mBot and then turn it back on, and off it goes. Five seconds later, it stops. Awesome. The mBot has performed as expected. Now, the next thing that I'd like to do is to get the mBot to turn left, right and then move backwards as well.

