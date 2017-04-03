# Section 5

---

## Chapter 28: Stopping at the end of the line

---

In this chapter you will learn about:

* How to make the mBot stop at the end of the line

---

In the previous chapter we programmed the mBot to follow a line. We noticed how it gets confused when it reaches the end of the line, though. There, through erratic movements and difference in traction between the two wheels it might even turn around and start following the line back to the beginning. In case we do want it to get back, we can understand that this is not an optimal solution.

In this chapter we will improve our program further by making it sense a marker, at the end of the runway, and then turn back by a certain amount of degrees and at a particular speed, and try to re-establish contact with the line and follow it all the way back to the start.

We will use therefore the proximity sensor as we have seen earlier.

Let's start editing the program of the previous chapter by creating a new variable named "distance\_to\_obstacle"  
 first, and then modify the program until we have it like shown in this image:![](/assets/Img.5.28.1.jpg)\[Image 5.28.1: The additions to the program\]

The additions:

\(1\) We assign to the new variable "distance\_to\_obstacle"  
 the reading from the proximity sensor.

\(2\) We add a new "if...else" block in the forever loop, and nest in the else \(3\) most of the "line\_sensor\_status" conditions.

What happens here is that the program gets two readings, one from the line follower module and one from the proximity sensor. If the latter is less than 10 cm. that means that the mBot has reached the object marking the end and it should stop setting its spead at zero. If not, it will keep on moving, either forward or by adjusting its route, depending on its position towards the line.

Let's "Upload to Arduino" and see all that in practice.

![](/assets/Img.5.28.2.jpg)

\[Image 5.28.2: The mBot stopping before the end marker\]

There's one more thing to do now: get the robot to turn around, as soon as it detects an obstacle, and go back where it started.

### Questions

Question 5.28.1: How can we have the mBot stop at the end of the line?

A. By keeping count of the distance already run, using the line follower sensor.

B. By sensing the distance left, using the line follower sensor.

C. By keeping count of the distance already run, using the proximity sensor.

D. By sensing a marker object place at the end of the line, using the proximity sensor.

_Answer: C_

