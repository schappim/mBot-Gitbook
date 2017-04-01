# Section 4

---

## Chapter 22: The "if" and "if...else" control structures

---

In this chapter you will learn about:

* How to have the mBot make desicions

---

In the last chapter we got ourselves an mBot that blinks its LEDs blue and red, depending on the distance between its ultrasonic sensor and a target object. That has given us understanding of how the ultrasonic sensor and the forever loop work.

In this chapter we will see how we can get the mBoard to make decisions, depending on sensor readings, like the ultrasonic sensor. Towards that goal, we're going to build a new program that, once more, uses the LEDs and the distance sensor only this time it turns the LEDs into a particular colour depending on the distance between a sensor and the target: green when it is far away, blue when it gets closer, red when it is too close.

In order to make desicions we use the "if" and "if...else" blocks that we can see in the image below:

![](/assets/Img.4.22.1.jpg)

\[Image 4.22.1: The "if" and "if...else" blocks\]

These two control blocks can evaluate a given condition and execute some nested instructions, depending on whether this condition is true or not. Blocks suitable to be used as conditions can be found in the \(green\) "Operators" family of blocks:

![](/assets/Img.4.22.2.jpg)

\[Image 4.22.2: Operators like these can compare values and be used as conditions\]

You will notice that such blocks have angular sides that make them fit in the condition spot, after the "if" word:

![](/assets/Img.4.22.3.jpg)

\[Image 4.22.3: Where to place the operator block\]

### A program that makes desicions

Let's create a new program: File &gt; New and use an if...else block to make a desicion

First, let's create a variable distance and by adding blocks and fit them together let's compose the program shown in the image below:

![](/assets/Img.4.22.4.jpg)

\[Image 4.22.4: The program\]

We notice that the if...else block is nested within the forever loop. Port3 refers to the port where the ultrasonic is connected on the mBot. We should always check such things in order to get the coresponding attributes right.

Here's how to read this program: Get a reading from the ultrasonic sensor and store it in the "distance" variable. Following, check this value, stored in "distance", and if it is greater than 30, then set all LEDs to green, else set them to blue. And all that, over and over again, since it's nested in a forever loop.

Now we can "Upload to Arduino" and check whether the mBot functions as expected: we place some obstacle in front of the sensor, at a distance somewhat greater than 30 cm. and the LEDs should turn to green. We move the object closer than 30 cm. and the LEDs should change colour and become blue.

### Expanding the program

Remember, though, that the original goal we set was to have three different colours and three different distance categories. Therefore, we will have to expand our program a little and here's how. Add an extra if...else block and all other necessary instruction blocks in order to have the program like this:

![](/assets/Img.4.22.5.jpg)

\[Image 4.22.5: The expanded program\]

In this new version, we first check whether the distance is greater than 30. If it is, we set the LEDs to green. Else we need to check further: if the distance is between 20 and 30 \(and we know it's 30 or less, or else we wouldn't have gotten this far\) then set the LEDs to blue, else the distance can be nothing else but 20 or less, and in that case set the LEDs to red. And all that, repeated again and again until we turn off the mBot.

Let's "Upload to Arduino" and check once more. Now, moving the object back and forth in front of the mBot, we should see the LEDs turn into three different colours, depending on the distance: green, blue and red.

### Exercise 4.22.1

Modify the program shown in image 4.22.5 so that instead of blue the LEDs shine amber.

Hint: remember how we learn, in previous chapters, to find the RGB codes of a specific colour.

### Question 4.22.1

What is the difference between an "if" and an "if...else" control block?

A. They have practically the same effect and can be used interchangeably.

B. The "if...else" block is more suitable to be used within loops.

C. The "if...else" block specifies what must happen when the condition is false, when the "if" block, doesn't.

D. Both B and C.

_Answer: C_

### Question 4.22.2

What kind of block can be used as a condition in an "if" block?

A. Anyone that is of the same block colour \(yellow\) as the "if".

B. A wait block.

C. A bare variable block.

D. One that has a shape that fits perfectly in the condition spot.

_Answer: D_

### Question 4.22.3

What is the way to have more alternative options in case an "if" condition turns up to be False?

A. There is no way since when a condition is False, the program always exits immediately the "if" control block.

B. We can combine more "if" and "if...else" blocks by nesting one into the other.

C. We can nest the "if" and "if...else" blocks so that they sooner or later can be evaluated to True.

D. We can use consecutive loops.

_Answer: B_

