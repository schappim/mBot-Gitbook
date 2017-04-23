# Section 5

---

## Chapter 27: Adding the motors

---

In this chapter you will learn about:

* How to use the motors to control the movement of the mBot using input from the line follower module

---

**This chapter contains hands-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will learn how to take input from the line follower module and use it to control the motors so that your mBot can move forwards while staying on the path that the line forms.

---

In this chapter you will continue to work on the program that you started in the previous chapter. You will make a small modification that involves the motors, so that your mBot can move.

If you consider what LEDs and motors have in common, we might say that they're both output devices, actuators: they both change the world in some way. The motors change the worlds by producing motion and the LEDs by producing light.

In that effect, the structure of the program, as it is at the moment, is fully capable to drive both LEDs and motors. All you have to do is place the motor movement instructions next to the LED ones.

Let's think about how to approach this modification.

### **Reacting to the line follower module status**

When the line-follower module reports "0", meaning that the mBot is fully within the track, then your mBot does not need to correct its course. It can simply continue to move forwards.

When the line-follower module reports 1, meaning that the right line sensor is outside , then your mBot should slightly to the left. This small correction will eventually get the right line sensor back over the black line, and the robot back on track, again.

When the line-follower module reports 2, meaning that that the left sensor is outside the line, then your mBot should turn slightly to the right, until the left sensor is again over the black line.

Finally, when the line-follower module reports 3, meaning that the mBot is fully outside the line, then your mBot should move backwards until it finds the line.

### **Expanding the program**

All the above is straightforward. Let's implement the necessary changes to the program.

First, introduce a variable to store the speed for the motors. Because you will be using the motor blocks in several locations in the program, it is better to define the speed at one place, and reuse it with the motor blocks.

Go ahead, create a new variable and call it "speed". Set it to a value, say 150.

---

**Did you know**

Remember, from earlier chapters, what is the meaning of the second parameter in the motor block? It is a number that ranges from 0 to 255. At 255, the speed of the motor is maximum. At 0, the motor is stopped.

When you work with motors, it is best to initially select a middle-of-the-range speed, instead of the two extremes. Once you have your prototype working, you can then experiment with higher or lower values as you optimise your program settings.

---

Next, insert the "\[run forward\] at speed" instruction block, that you can find in the "Robots" blocks group.

![](/assets/Img.5.27.1.jpg)

\[Image 5.27.1: The "\[run forward\] at speed \[0\]" instruction block\]

You can change the first attribute of this block to make the mBot move either forwards or backwards and turn either left or right. As for the second attribute, set it to variable "speed" that you created earlier.

Make the appropriate changes to your existing program so that eventually it matches the program in Image 5.27.2.![](/assets/Img.5.27.2.jpg)\[Image 5.27.2: This version of the program includes the motor control blocks \]

The numbers in Image 5.27.2 refer to the following notes:

\(1\) Set the variable "speed" to 150.

\(2\) Insert the motor control blocks.

Every time the loop starts, the program reads the line follower module status and uses this information to direct the motion that the motors should perform. If the module returns "0" then the mBot just moves forwards. If the module returns a value that indicates that one of the sensors is outside the line, then the mBot will turn left or right to eventually get it back on the track. If both sensors are outside the line, then the mBot will move backwards, until it to detects the line again.

Get ready to test the program now.

* First we make sure that there is a line for your mBot to follow, on a sufficiently large surface, like the floor.
* Then, upload the program to your mBot. When the upload completes switch it off, and place it at the beginning of the line.
* And then, switch on.

Did your mBot behaves as expected? Did it follow the line?

![](/assets/Img.5.27.3.jpg)\[Image 5.27.3: The mBot at start position\]

As can be seen in the image above, you can place obstacles to mark the start and finish of the runway. These will be useful in the improvements that you will apply to the program in the next chapter.

If your mBot behaved as expected, you must have noticed that it followed the line by constantly adjusting its direction of movement, until finally it reached the end of the line. There, the mBot didn't stop, since you didn't include such behaviour in the program. Instead it made erratic movements in its effort to get its line sensor module back on the line, by moving backwards. Eventually, due to difference in traction between the wheels, it is possible that your mBot managed to turn enough to get back on track.

We can actually improve the way that the mBot behaves when it reaches the end of the line so that it can get back on the track much faster that with the current version. You can use the proximity sensor so that the robot can detect the end of the line, by sensing the obstacle we have placed there. After it detects an obstacle, you can program it to do a U-turn \(i.e. a 180 degree turn\) and quickly find itself back on the track. This is what you will do in the next chapter.

And of course, let's remember to save the project, before continuing!

---

#### Question 5.27.1: What will happen when the mBot reaches the end of the line, executing the program in image 5.27.2?

A. It will stop moving.

B. It will perform a U-turn by executing the corresponding U-turn block.

C. It may perform a U-turn due to difference in traction between the wheels.

D. It will go on eventually crashing on some obstacle found in the way.

_Answer: C_

---

#### Question 5.27.2: Experiment with the motor speed value that is stored in variable "speed". What is the highest value that you can set this variable at with the mBot still able to follow your line?

Max speed:  \_\_\_\_\_\_\_\_

Answer: in my experiments, with the line in Image 5.27.3, the max speed was around 200.

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] Your mBot can follow the line on the floor

\[   \] You the way that the mBot turns in relation to the values that the line following module reports

\[   \] You understand the difficulty that the current version of the program has to help the mBot find the line when it reaches the end of the line

\[   \] You understand the relation between the motor speed and the ability of the mBot to follow the line

---

