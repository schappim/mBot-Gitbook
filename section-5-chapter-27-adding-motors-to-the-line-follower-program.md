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

~~~~~~~~~~~~~~~~~~~~~~~~~~~~



If we use a turning correction for the condition of the rubber being completely outside the line, then we need to remember which way the line was when we lost contact with it. That is possible but it's slightly harder to implement. Let's ignore that possibility for now or that possible solution. An easier thing to do is to move backwards because what really only moves forward at some point is going to lose the lines.

There's a good chance that the line is behind it. What we do then is just reverse the robot until it re-establishes contact with the line. Let's do that. Let's grab the moving block. Just put it here in place in the last L's. Instead of forwards, let's make that backwards. Again, we can use 150 as a value to get started with. That looks good enough as a version that we can actually take and test in the field in real life.

I'd like to do one small modification with improvement before I upload it. That is to do with this repetition of 150 for all of the speeds. That's 150, 150, 150 and 150. I can improve that by replacing these occurrences of the value 150 with a single variable. Let's go to data and blocks and create a new variable and call it speed. I want to set the speed to 150 right at the beginning.

Then replace all the fixed occurrences of the value 150 with a variable speed. This will make it easy for me to adjust the speed without having to expend too much effort. It turns out that the robot is having a hard time staying on the track. I can decrease the speed to give it a bit more time to sense its position on the track. What now we can do is to increase the speed to see how fast the import can go before it starts having trouble staying on the track.

All right, time to try this out. I'm going to connect to com six and upload to the Adreno. It's uploading. As soon as it finishes the upload, it will start running the program. There you go.

\[background noise\]

\[laughs\] It reached the end and then, of course, then it lost it because it reached the edge of this piece of track that I've got on my table. I'm going to turn it off and go over to the track that I've got on the floor and test it on the track. Here we are, on the floor of assembled a track from the pieces of track that are printed on A4 sheets of paper. Let's see if the robot can actually follow the curves.

I also would like to know what happens once it reaches the end. Turn it on and off it goes. Takes a curve nicely. Goes around the bend and reaches the end. What happens at the end? Looks like there is a little bit or turning happening. That might help the robot come back all the way around. There are 180-degree turn and see if it will make it around. Yes, it did and come back where it started. Reaches the other end. You can see that according to this program I guess it's only supposed to reverse back.

You can see that according to this program I guess it's only supposed to reverse back. You can see there's a slight right turn every time that it reverses. That really is because its wheels are slipping. That's one wheel on the paper and the other one on the floor and because of the difference in traction, eventually the robot will turn and find its way around and re-establish contact with the line.

The next iteration can improve on that. What I'd like to do in the next iteration of the program, is to use the sensor, is to use the proximity sensor so that the robot can detect by itself the end of the line. Thanks to the little obstacles that I've got here. Then use this information to do a U-turn and come back where it started. Without spending so much effort there and energy trying to do the turn. Okay, let's go back to the computer and work on that improvement next.

