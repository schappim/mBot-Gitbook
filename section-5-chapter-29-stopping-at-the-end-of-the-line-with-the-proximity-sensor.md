# Section 5

---

## Chapter 28: Turning around at the end of the line

---

**In this chapter you will learn about:**

* How to get the mBot to stop at the end of the line
* How to get the mBot to make a U-turn

---

**This chapter contains hands-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will learn how to improve the behaviour of your mBot when it reaches the end of the line.

---

In the previous chapter you programmed the mBot to follow a line. You noticed, though, that it is not able to react well to the end of line condition. When it detect the end of the line, it will simply reverse in an attempt to get back on the line. If there is a small difference in traction between the two wheels, after a while the mBot will actually turn around and continue to follow the line towards the opposite direction. Obviously, this is not an optimal solution to the end of line condition.

In this chapter, you will work to improve the functionality of your line following mBot so that it reacts better to the end of line condition.

### The difference between "end of line" and "out of line"

To make it possible for the mBot to detect the end of the line so that it can react appropriately, you need to understand that there are two possible conditions that involve the line sensor reporting status 0:

1. The mBot has lost contact with the line while it is travelling on it. This can happen, for example, as it is negotiating a sharp turn.
2. The mBot has lost contact with the line because it has reached its end.

As far as the line follower module is concerned though, in both cases it will return status 0, making it impossible for the mBot to differentiate between the first or the second condition. To be able to do so, the mBot needs additional information.

That's where the ultrasonic proximity sensor becomes useful. You can use information provided by the ultrasonic sensor to supplement the information provided by the line follower module so that the mBot can differentiate between condition one and condition 2.

---

**Did you know**

Using data from multiple sensors is a very common practice in machines like self-driving cars, quadcopter drones, and home security systems, to name a few. By combining data from multiple sensors, you program can calculate a better representation of what is going on in the environment, compensate for errors, and improve its accuracy.

---

### Improve your program

Let's improve your program by modifying it so that it can detect a marker object \(like a small box\) at the end of the line, using the ultrasonic sensor. You will program your mBot so that when it detects this marker it will turn back by a certain amount of degrees and at a particular speed, and try to re-establish contact with the line. When this happens, it will simply follow it all the way back to the start.

Creating a new variable named "distance\_to\_obstacle", and then modify the program until you have it like shown in Image 5.28.1:![](/assets/Img.5.28.1.jpg)\[Image 5.28.1: The additions to the program\]

These are the additions \(the numbers correspond to the annotations in Image 5.28.1\):

\(1\) Read a value from the ultrasonic sensor connected to port 3 and store it in variable "distance\__to\_obstacle"._

\(2\) Add a new "if...else" block in the forever loop and nest in the "else" segment \(3\) the "line\_sensor\_status" conditions from the previous version of the program.

This program gets two readings: one from the line follower module and one from the ultrasonic sensor. If the latter is less than 10 cm. that means that the mBot has reached the object marking the end and it should stop by setting its speed at zero. If not, it will keep on moving, either forward or by adjusting its route, depending on its position towards the line \(like the small grey box in Image 5.28.2\).

![](/assets/Img.5.28.2.jpg)

\[Image 5.28.2: The mBot stopping before the end marker\]

Upload the new program to your mBot to see all that in practice.

Great, your mBot now can detect the end of the line, and stop.

There's one more thing to do now: get the mBot to turn around, as soon as it detects an obstacle, and go back to where it started.

### Making a U-turn

You are now getting closer to having the mBot deal with the end of line issue.

The next operation you should include for the end of line condition is to turn the mBot around enough so that it re-establishes contact with the line and then continue to move in the opposite direction.

There are multiple ways to achieve the same result, programmatically, and here is one possibility:

![](/assets/Img.5.28.3.jpg)

\[Image 5.28.3: The modification to the program\]

You can replace the previous "run forward at speed 0" with these two blocks \(1\) :

* turn right at speed 255
* wait 0.5 secs

The speed and wait values here have worked in a previous experiment but you can always try different values and test them until you like the way that the mBot executes the U-turn.

Once you complete the necessary modifications to your program, go ahead and upload it to your mBot. Place your mBot at the beginning of the line and let it start its journey. Pay special attention to what it does once it reaches the end of the line. Instead of stopping, it should now turn around and start following the line back to the start. If you have placed another object there, it should loop the runway endlessly.

Keep in mind that there is always space for improving the way the mBot executes the U-turn and you can try different values for speed and time until you have a satisfactory manoeuvre.

Remember to save a program when we are done with applying modifications we mean to keep. You will continue your work on this program in the next chapter.

---

**Question 5.28.1: How can you program the mBot to stop at the end of the line?**

A. By keeping count of the distance already run, using the line follower sensor.

B. By sensing the distance left, using the line follower sensor.

C. By keeping count of the distance already run, using the proximity sensor.

D. By sensing a marker object placed at the end of the line, using the proximity sensor.

_Answer: D_

---

**Question 5.28.2: What is one way to implement a U-turn?**

A. By having the mBot turn around for a specific portion of time.

B. By having the motors start spinning backwards.

C. By having the motors keep spinning forwards.

D. By having the mBot turn 45 degrees to the right.

_Answer: A_

---

**Question 5.28.3: What is the smallest distance to the end of line object that you can set in your program, that still enables your mBot to turn around? Experiment with your mBot to find out.**

Smallest distance to the end of line object that works with your mBot: \_\_\_\_\_\_\_\_\_

_Answer: this may vary, but it should be around 5 cm._

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] Your mBot can detect an object that you have placed at the end of the line

\[   \] Your mBot can stop moving when it detects an object that you have placed at the end of the line

\[   \] Your mBot can detect an object that you have placed at the end of the line, turn around and continue to move in the opposite direction

---



