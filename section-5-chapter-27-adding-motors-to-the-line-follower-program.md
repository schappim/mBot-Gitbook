# Section 5

---

## Chapter 27: Adding the motors

---

In this chapter you will learn about:

* How 
* How
* How 

---

It's about time to get those motors moving.

We are going to work on the program that we created in the previous chapter and just modify it slightly.

If we think about what is the similarity between an LED and a motor, we might say that they're both output devices, actuators: they both modify the world in some way. The motor by producing motion and the LED by producing light. 

In that manner, the structure of the program, as we have it by now, is ready to go. All we have to do is place the motor movement instructions next to the LED ones.

Let's think about how to approach it, now.

When the line sensor reports a zero, we know it must  it looks like the inboard is within the track, fully within the track and all it's going to do really is just to move forwards.

Actually, the modifications are smaller than you might think.

It doesn't need to adjust its course. That means that all it's got to do is to just get it to run forwards, like that. Run forwards and let's give it a speed. Let's make it say, I'll make it 150 actually. 150. Now, let's see what happens when the sensor is reporting a one. The sensor reports a one when it is at this position. Sensor number two is outside the black line. Sensor number one is inside the black line.

Now, what is it that we need to do if the sensor reports a one at this position? What we need to get the robot to turn towards the left to do a slight left turn, like that. What we need to do then is to get the motor at this position here to turn left at a particular speed. Let's make it also a 150, like that. What's left to do? Let's say that the sensor is reporting a two.

A two means that sensor number two is inside the black line. Sensor number one is outside the black line. What does the robot need to do in order to get back in track? It needs to move slightly towards the right. It needs to make a small right turn. Let's do that.

Let's grab this block and move it down here where we've got the condition for lines as the status equals two and make that a right turn. I give a speed of also, make it 150. At this point, I don't know if the speeds that I'm assigning here to the motors are reasonable or not because the speed depends on things such as the shape of the line. We can imagine it's just like a car.

A car can run faster if it's got a long stretch of straight road ahead of it. Then it's got to slow down if it has to go through a bend. It's the same thing with the robot. Robot can have higher speed if it simply has to travel at a straight line. When it encounters a curve, it needs to slow down or needs to go to a slower speed.

I will have to test it later on the actual track. It will be on the floor to see the speeds that I'm assigning here are correct. The last one is a little bit tricky. This L's covers the condition where the rubber is fully outside the black line. What do you think that the robot should do now to try and find the black line and get back in it? What would it do? Think about it.

There are few things it can do. It can turn either one way or another trying to find the line again. The problem with turning is that it needs to know which way to turn. If it turns towards the left and you can see that things are getting even worse because it's going further away from the line. If it turns towards the right, then eventually it will hit the line and will be able to continue then.

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



