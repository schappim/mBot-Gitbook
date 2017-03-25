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





 There's port M one and port M two. To show you how to use the motors, I'm going to create a new programs or file and then select new. I'm going to go to the robots section of the scripts tab. Just like in the previous example, we'll start by dragging and dropping the mBot program block onto the canvas. Let's put it here.

There are couple of blocks that allow you to control the motors. There's this one here and then there's this one here. The first one is the one that we'll be using today. In this crash course, it allows you to get your MBot to move forwards backwards or to turn right or left. The second one allows you to control independently one or the other motor, so either the motor that is connected to connector M1 or to connector M2. This is a little bit more involved.

For now, I'd rather just leave it alone while we familiarize ourselves with the more typically used blocks. I'm going to attach the run forward block to the mBot program header block. This block requires you to configure two attributes. First is the direction of the move, we've already selected forwards, and then the speed. The speed can take any number between minus 255 and 255 positive.

Obviously, minus means that when the block is configured to run forwards and you have a negative speed, then obviously your robot is going to move backwards instead of forwards and vice versa. If you have the block configured to run backwards and you use a negative speed, then it's going to move forwards. Keep that in mind. I'd like to get my robot to move forwards at a particular speed. Let's make it 100.

Now, this number does not mean anything in particular. Does not mean something like centimeters per second or kilometers per hour or anything like that. It's just a number and then how fast it goes really depends on how depleted your batteries are or whether there's some heavy load on the robot things, like that. It's just an arbitrary number to allow us to get the motors to spin at a particular speed.

You can find **\[unintelligible 00:03:24\]** of course, you don't have to select one of the values from the drop-down. You can go for anything else in between those values. So we can go for, say, 125. Let's see what the effect of this is. I've got my upload to the Arduino programming side of the M block application already displaying. You can see that as I dropped the movement block onto the canvas here, then the setup method of the Arduino sketch updated itself with the value that I prescribed, with the value that I typed in, 125 and 125 here on the block.

Let's upload that. First, I'll make sure that I'm connected to the appropriate com port. You can see that before the break, I had com four, now it's com six. It's because I turned off and then back on the mBot and that assigned it automatically to a new port. It doesn't really matter. I just reconnect to com six, done, and upload to the Arduino which means upload to the mBot. I'm going to hold it up a little bit because this is going to start running the sketch immediately. The wheels are going to start spinning. If I leave it on the table, it's just going to run off the table and fall on the floor. Writing, reading, there you go.

When I work with the mBot on my table, I often just turn it upside down so that I don't have to chase the mBot around my table. Now, this is going to continue spinning indefinitely because I haven't configured my program to do something like stop the wheels from spinning after a particular number of seconds. It's just going to go on indefinitely.

How about we get the robot to move forwards at this particular speed for five seconds and then I'd like it to stop. How do we do that? You may remember from the experimentation we did earlier with the sprite, that there is a function called wait. Go back to the control section of the scripts tab and there's a wait block here. I'm going to drag that and put it after my run block. I configured this to operate for five seconds. I'm going to include a wait block here that waits at this location of the program for five seconds .

Now, go back to robots, pick the run forwarded speed block again. But this time I'm going to leave it at zero because zero means that the motors have stopped spinning. Let's upload again to the Arduino. You can see that the sketch has been updated with the new command. Here's my delay five. Here's the move and the speed here is zero. Upload it. Uploading, writing, reading there you go, and stopped.

There was -- I think you can get about five seconds and the wheels then stopped after five seconds because it reached the last around forward statement which was asking -- which was instructing the robot to stop from moving. Now, what I'll do is I would like to test my robot on the floor so I can actually see it moving. To do that, I simply remove the USB cable. Since I've got the battery connected the **\[unintelligible 00:07:54\]** is still powered and I'm going to turn it off. Now, when it turn it back on, the program is always stored inside the Arduino that runs the mBot and execute automatically. It will execute one time and then it will stop. If I want to re-execute the program, I've got to power cycle the mBot. I've got to turn it off and then back on.

Another way to get your mBot to execute the program again is to reset it. There is a reset button right here, right inside this little hole. You need to use a tool to be able to reach there. I'm going to use my tweezers. Use the tweezers and set it inside the little opening of the case. Press the button and then the program will executes again. That's a alternate way of running a resident sketch instead of power cycle.

The reset button is the same as this reset button on the Arduino board. The effect is exactly the same. It will re-execute the program that is stored on the chip on the out maker. Let's take my mBot over to the floor where I've already set the track that eventually the mBot will be following to see it moving forwards for five seconds and then stopping. I will turn off the mBot and then turn it back on, and off it goes. Five seconds later, it stops. Awesome. The mBot has performed as expected. Now, the next thing that I'd like to do is to get the mBot to turn left, right and then move backwards as well.

