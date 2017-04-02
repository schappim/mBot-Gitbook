# Section 5

---

## Chapter 28: Stopping at the end of the line

---

In this chapter you will learn about:

* How to have the mBot stop at the end of the line

---

In the previous chapter we programmed the mBot to follow a line. It gets a bit confused when it reaches the end of the line, it doesn't quite know what it does. Its programming is telling it to just reverse. And, hopefully, because of the difference in traction between the two wheels. At some point, it might turn around far enough to be able to go back where it started. Obviously, that's not an optimal solution to this problem, there's too much chance.

I'd like to make a small recommendation, a small improvement. I would like to set a marker for the robot to be able to detect so that once it reaches that marker, it knows it needs to be a little bit more radical with its behavior. And instead of simply reversing, to perhaps turn by a certain amount of degrees or at a particular speed and then try to re-establish contact within line like that.

What I'd like to do in order to get started with that idea and try it out, is to get the robot to simply detect an obstacle in front of it and if that obstacle is close enough to simply stop, instead of trying to just reverse and then randomly return, just stop and then we'll figure out as a later iteration of how exactly to do the turn.

As we have seen before, we can read data from the proximity sensor and then use that data to determine what the robot should do. As a first modification to the sketch that we started in the previous part, is to create a new variable, we'll call this variable distance to obstacle, just to be clear as to what this variable is for. Now, we need to read the distance to an obstacle ahead, and for that, we need to use the ultrasonic sensor. There it is. Let's go to data and blocks, and just like at the beginning of the forever block, I am setting the line sensor status, that's also a good place to set a distance to obstacle to whatever value the ultrasonic sensor is reporting.

The next thing that we need to do is to use this information to tell the robot whether it should actually stop or not. Take a few seconds to think about how you can deal with this. What would you do? That sounds like a need here for the robot to make a decision, right? That sounds like a job for an if-else statement. Let's go to control then. The easiest way to deal with this is to use another if-else statement, you can just put it down here where there's a bit of space or make that part of the program to disappear, just make a bit more space for the program which is now starting to get big.

I'll put that block here for the time being. What I'd like to do is to get information from the sensor and then compare the distance to obstacle to let's say 10 cm. If the robot has reached within 10 cm of an obstacle ahead of it, I'd like it to stop right there. Let's go to the operators and pick this operator here, less than, and go to data blocks and choose the distance to variable, sorry, the distance to obstacle variable, and put a fixed number 10 here. So, if the distance to obstacle is less than 10, then we would like it to stop.

So how do we stop a robot? Is we tell it to stop its motors. So run forward at speed zero. Otherwise, I would like it to just do the rest as normally. So I can just drag this whole block here, this whole thing, the whole block, and just move it inside the else statement, like that. And then take this new block and put it here, inside the forever loop, just like that. We can test this now to see if it actually works. What I expect to happen is that if the obstacle is set 10 cm or less for the motors to stop moving, otherwise, for the robot, it'll just behave like it did in the previous iteration of the program.

Let's upload to the Arduino and it will connect it and turn it on. I'm going to flip it upside down so that the wheels don't cause the robot to disappear under the table. So, upload to Arduino. Okay. Let's see if it works. All right, yes, it looks like it is. My hand is within that 10 cm range that I've specified that the motors should just stop working, and you can see that they wheels have stopped working.

Let's going to try this out on the actual line. Disconnect it, I'll turn it off. Here, we are at the track, and I've got the mBot set at the beginning of the track. At either end of the truck, I've got small cardboard boxes to play the role of the obstacle. I'm going to turn it on and see what happens. If it goes just like before, nothing has changed in that respect, as long as there's no obstacle within 10 cm, the robot will just keep going. Whoop, there you go, it stopped, detected the obstacle and it stopped. Awesome.

There's one more thing to do now, and that is to get the robot to turn around and go back where it started as soon as it detects an obstacle. Let's try that next



