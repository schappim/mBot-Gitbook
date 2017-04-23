# Section 5

---

## Chapter 29: Using a button to start and stop

---

**In this chapter you will learn about:**

* How to use the on-board button using the "on board button" block

---

**This chapter contains hands-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will learn how to use the on board button.

---

Your mBot's mCore controller includes a button that you can use in your programs. You program can read the state of the button, determine if it is pressed or released, and trigger whatever functionality you wish accordingly. 

You will find this button on the front right side of your mBot \(see Image 5.29.1\). You can program it, for example, so that when the robot is powered on, the wheels either start or stop, by pressing it. Again, there are multiple ways to implement this behaviour and in this chapter we are going to implement one of them. 

![](/assets/Img.5.29.1.jpg)

\[Image 5.29.1: The board button\]

Let's continue with the program your worked on in the previous chapters.

You wish to implement a button function that treats the button as a toggle switch. When you press the button, the wheels will stop, and the mBot will remember this so that the wheels continue to be stopped. When you press the button again, the wheels will start spinning \(because their previous state was stopped\). The mBot will remember this and continue to spin them, until you press the button again, in which case the wheels will stop. So, a toggle switch has memory, which allows the mBot to remember the last state of the button \(wheels spinning or not spinning\).

Let's implement this functionality.

Start by creating a variable named "button\_toggle" that will be used to hold the status of the board button. You will assign just two values to this variable:

* **-1** for having the wheels spinning
* **1** for having the wheels stopped

First, and since we mean for the mBot to have the wheels spinning when the program is loaded, let's initialize this variable to -1, at the very start, like this:

![](/assets/Img.5.29.2.jpg)

\[Image 5.29.2: Initializing the "button\_toggle" variable\]

For the rest, when the board button is pressed, we need to invert its value, assigning the opposite status to it. One simple way to do that is by multiplying its value by -1. If it was -1, it will now become 1, and vice versa. Here's how to do that:

![](/assets/Img.5.29.3.jpg)

\[Image 5.29.3: Inverting the status of the board button\]

Here, if the board button is pressed, then we set the opposite value to the "button\_toggle" by multiplying its current value by -1. The "on board button \[pressed\]" can be found in the \(navy blue\) "Robots" segment.

One last thing we need to do is check the status of the board button \(stored in variable "button\_toggle"\) using an if block, like this:

![](/assets/Img.5.29.4.jpg)

\[Image 5.29.4: Checking the status of the board button\]

If it is 1, we should proceed with all the lot of instructions we created previously for trying to keep the mBot on track. If it is -1, we should just stop the wheels. That means that we should move all these instructions within the if block \(when the board button status is 1\), and add a stop instruction \("move forward at speed 0"\) within the else \(when the board button status is -1\)

Here's how to combine these new instructions in the program:

![](/assets/Img.5.29.5.jpg)

\[Image 5.29.5: The new modifications\]

It just needs some extra attention to get all this right. Once we get the program like we see it here, in the image above, we can "Upload to Arduino". Now, every time we press the button, the wheels must either stop or start moving, depending on their current status.

That is the last bit of functionality that we introduce to the mBot, at least in the context of this crash course. We need to look into one last thing, though. We notice that this program has grown to quite a large size.

Next, we will see how to break down this long program into smaller parts, called "functions", that are easier to manage.

### Questions

Question 5.29.1 What is the use of the board button?

A. It is meant by default to start and stop the wheels.

B. It starts and stops the power supply to the mBot.

C. It has a general use and it can be programmed to perform assorted actions.

D. Both A and B.

_Answer: C_

