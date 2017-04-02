# Section 5

---

## Chapter 27: Adding the motors

---

In this chapter you will learn about:

* How 
* How
* How 

---

It's about time to get those motors moving. We are going to work on the program that we created in the previous chapter and just modify it slightly.

If we think about what LEDs and motors have in common, we might say that they're both output devices, actuators: they both modify the world in some way. The motor by producing motion and the LED by producing light.

In that effect, the structure of the program, as we have it by now, is ready to go. All we have to do is place the motor movement instructions next to the LED ones.

Let's think about how to approach it, now.

### **Reacting to the readings**

When the line follower module reports a zero, we know that the mBot must be fully within the track and all it has to do really is just to move forwards. No need to adjust its course.

When the line follower module reports a one, that means that the right sensor got outside the line and we should turn the mBot a little to the left, to get both sensors inside the line and the robot back on track.

When the line follower module reports a two, that means that the left sensor got outside the line and we should turn the mBot a little to the right.

Finally, when the line follower module reports a three, then the mBot got way outside the line and maybe the best idea is to get it to move backwards in hope to meet the line again.

### **Expanding the program**

All the above seems straight forward and here is how we can implement it.

First of all we need a variable in order to set a fixed speed, for the motors, that we can use within the program. So, let’s create a variable and call it "speed", and set it to some speed, say 150.

For the rest we will need the "\[run forward\] at speed \[0\]" instruction block, that can be found in the "Robots" instructions family.

![](/assets/Img.5.27.1.jpg)

\[Image 5.27.1: The "\[run forward\] at speed \[0\]" instruction block\]

The first attribute of this block can be altered to make the mBot move either forwards or backwards and turn either left or right. As for the second attribute, we will set it to variable "speed".

Here is how we must modify the program:![](/assets/Img.5.27.2.jpg)\[Image 5.27.2: The program\]

The modifications are pointed at, to make it easier to spot them:

\(1\) is where variable "speed" is set to 150.

\(2\) is where the motor moving block is added

What happens here is that every time we get a reading from the line follower module, we decide as to how the mBot must move. If things look good, it just moves forwards. If either one sensor seems to have gotten outside the line, we turn the mBot, to get it back on track. If both sensors have gotten outside the line, we move the mBot backwards in the hope to meet the line again, since the best chance is that the line is behind it.

Let's get ready to test the program now:

* First we make sure we have composed a line runway on some spacy surface, most probably on the floor.
* Then we connect the mBot to the computer and "Upload to Arduino" and then we can switch it off, so that we can place it at the begin of the line.
* And then, we can switch in on and see if it behaves as expected.

![](/assets/Img.5.27.3.jpg)\[Image 5.27.3: The mBot at start position\]

As can be seen in the image above, we can place obstacles to mark the start and finish of the runway. These will prove useful in the improvements we are going to apply to the program, in the next chapter.

If we turn the mBot on, we will see it get going, following the line by constantly adjusting its route, until finally it reaches the end of the line. There, we will notice that the mBot doesn't stop, since we didn't include such a behaviour in the program. Instead it will make erratic moves that might even get it to make a U-turn, eventually, due to difference in traction, between the wheels.

We can actually improve the program even further by using the proximity sensor so that the robot can detect by itself the end of the line, by sensing the obstacle we have placed at the end of the line. And then even make a U-turn to get back to where it started. We will handle all this in the next chapter.

