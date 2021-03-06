# Section 4

---

## Chapter 22: The "if" and "if...else" control structures

---

**In this chapter you will learn about:**

* How to have the mBot make decisions
* How to use the "if" and "if...else" control blocks
* How to "nest" control blocks into other such blocks
* What a "condition" is and how it affects the flow of the execution of a program

---

**This chapter contains hands-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will learn about the "_if_" and "_if...else_" control structures.

---

In the previous chapter you programmed your mBot to control its RGB LEDs in accordance to the distance between its ultrasonic sensor and an object in-front of it. This experiment has helped you to understand how to use the ultrasonic sensor and the "forever" loop control structure.

In this chapter you will learn how to program your mBot to make decisions. The decision will depend on sensor readings, such as the ultrasonic sensor. To achieve this kind of functionality, you will compose a new program that, once again, will use the LEDs and the distance sensor.

But this time, it will turns the LEDs into a particular colour depending on the distance between a sensor and the object: green when it is far away, blue when it gets closer, red when it is close.

In order to make decisions we use the "if" and "if...else" blocks that we can see in the image below:

![](/assets/Img.4.22.1.jpg)

\[Image 4.22.1: The "if" and "if...else" blocks\]

You will find the "if" and "if...else" blocks in the Control block group.

These two control blocks can evaluate a given condition and execute some nested instructions, depending on whether this condition is true or not. Blocks suitable to be used as conditions can be found in the \(green\) "Operators" group of blocks:

![](/assets/Img.4.22.2.jpg)

\[Image 4.22.2: Operators like these can compare values and be used as conditions\]

Notice that such blocks have angular sides that make them fit in the condition spot, after the "if" word:

![](/assets/Img.4.22.3.jpg)

\[Image 4.22.3: Where to place the operator block\]

### A program that makes decisions

Create a new program.

First, create a new variable named "distance" and add the appropriate blocks so compose the program that you can see in Image 4.22.4.

![](/assets/Img.4.22.4.jpg)

\[Image 4.22.4: The program\]

Notice how the "if...else" block is nested within the forever loop?

---

**Question 4.22.1: In the program of Image 4.22.4, which port is the ultrasonic sensor connected to?**

A. 1

B. 2

C. 3

D. 4

_Answer: C_

---

Try to read this program to understand what it will do before you upload it to your mBot.

1. Get a reading from the ultrasonic sensor and store it in the "distance" variable. 
2. Check the value stored in "distance", and if it is greater than 30, then set all LEDs to green, else set them to blue. 
3. Repeat, forever.

Upload your program to your mBot and check whether the mBot functions as expected. Place an obstacle in front of the sensor, at a distance somewhat greater than 30 cm., and the LEDs should turn to green. Move the object closer than 30 cm and the LEDs should change colour and become blue.

### Expanding the program

The original goal we set, though, was to have three different colours and three different distance categories. Therefore, you will have to expand our program a little more.

To do this, you can use multiple "if...else" blocks, nested one inside another. Do that, and try to compose the program that you can see in Image 4.22.5.

![](/assets/Img.4.22.5.jpg)

\[Image 4.22.5: The expanded program\]

In this new version, the program will first test whether the distance is greater than 30. If it is, it will set the LEDs to green.

If not, if will do a second test: it will test if the distance is between 20 and 30 \(it already knows that it's less than 30, or else it would not have gone this far in the program\) then set the LEDs to blue. If the last test turns out to not be true, then the program will set the LEDs to red since it will have determined that the distance is less than 20 or less.

This process is repeated forever until you turn off the mBot, reset it, or upload a new program.

In larger programs, It is not unusual to have layers of control blocks nested within other control blocks in order to implement complicated control structures.

Upload your program to your mBot and test it. Now, moving the object back and forth in front of the mBot, you should see the LEDs turn into three different colours, depending on the distance: green, blue and red.

Save the program or just keep it open if we would like to proceed immediately with the next chapter where you will add the use of the buzzer into it.

---

#### Question 4.22.2: Modify the program shown in image 4.22.5 so that instead of blue the LEDs shine amber.

Hint: remember how we learned, in previous chapters, to find the RGB codes of a specific colour.

_Answer: modify the values of the "set led on board" block from \(0, 0, 0\) to \(255, 191, 0\) \(red, green, blue\)._

---

#### Question 4.22.3: What is the difference between an "if" and an "if...else" control block?

A. They have practically the same effect and can be used interchangeably.

B. The "if...else" block is more suitable to be used within loops.

C. The "if...else" block specifies what must happen when the condition is false, when the "if" block doesn't.

D. Both B and C.

_Answer: C_

---

#### Question 4.22.3: What kind of block can be used as a condition in an "if" block?

A. Any that is of the same block colour \(yellow\) as the "if".

B. A wait block.

C. A bare variable block.

D. One that has a shape that fits in the condition spot.

_Answer: D_

---

#### Question 4.22.4: What is the way to have more alternative options in case an "if" condition turns up to be False?

A. There is no way since when a condition is false, the program always exits immediately the "if" control block.

B. We can combine more "if" and "if...else" blocks by nesting one into the other.

C. We can nest the "if" and "if...else" blocks so that  sooner or later they can be evaluated to True.

D. We can use consecutive loops.

_Answer: B_

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] You know how use the "if" structure

\[   \] You know how to use the "if...else" structure

\[   \] You know how to nest an "if...else" structure inside another "if...else" structure

