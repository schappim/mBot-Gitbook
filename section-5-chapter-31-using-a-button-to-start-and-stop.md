# Section 5

---

## Chapter 29: Using a button to start and stop

---

In this chapter you will learn about:

* How to program the board button to start and stop the wheels

---

On the mBot, on the right side, there is a little board button that can be programmed to cause a reaction by the mBot. We can program it, for example, so that when the robot is powered on, the wheels either start or stop, by pressing it. Again, there are multiple ways to implement this behaviour and in this chapter we are going to see one.

![](/assets/Img.5.29.1.jpg)

\[Image 5.29.1: The board button\]

Let's continue with our program of the previous chapters and create a variable named "button\_toggle" that will be used to hold the status of the board button. We will be assigning just two values to this variable:

**-1** for having the wheels on

**1** for having the wheels stopped

First, and since our program will have the wheels spinning when loaded, let's initialize this variable to -1, at the very start of the program like this:

![](/assets/Img.5.29.2.jpg)

\[Image 5.29.2: Initializing the "button\_toggle" variable\]

For the rest, when the board button is pressed, we need to invert its value, assigning the opposite status to it. One simple way to do that is by multiplying its value by -1. If it was -1, it will now become 1, and vice versa. Here's how to do that:

![](/assets/Img.5.29.3.jpg)

\[Image 5.29.3: Inverting the status of the board button\]

Here, if the board button is pressed, then we set the opposite value to the "button\_toggle" by multiplying its current value by -1. The "on board button \[pressed\]" can be found in the \(navy blue\) "Robots" segment.

One last thing we need to do is, is check the status of the board button \(kept in variable "button\_toggle"\) using an if block, like this:

![](/assets/Img.5.29.4.jpg)

\[Image 5.29.4: Checking the status of the board button\]

If it is 1, we should procceed with all the lot of instructions we created previously for trying to keep the mBot on track. If it is -1, we should just stop the wheels. That means that we should move all these instructions within the if block \(board button status = 1\), and add a stop instruction \("move forward at speed 0"\) within the else \(board button status = -1\)

Here's how to combine these new instructions in the program:

![](/assets/Img.5.29.5.jpg)

\[Image 5.29.5: The new modifications\]

It just needs some extra attention to get all this right. Once we got the program like we see it here, in the image above, we can "Upload to Arduino". Now, every time we press the button, the wheels must either stop or start moving, depending on their current status.

That is the last bit of functionality that we introduce to the mBot, at least in the context of this crash course. We need to look into one last thing, though. We notice that this program has grown to quite a large size.

Next, we will see how to break down this long program into smaller parts that are easier to manage, called "functions".

### Questions

Question 5.29.1 What is the use of the board button?

A. It is meant by default to start and stop the wheels.

B. It starts and stops the power supply to the mBot.

C. It has a general use and it can be programmed to perform assorted actions.

D. Both A and B.

_Answer: C_

