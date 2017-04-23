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

* "**-1"** for having the wheels spinning
* "**1"** for having the wheels stopped

First, and since you'd like for the mBot to start moving on the line immediately when the program is loaded, initialize this variable to -1, at the very start, as you can see in Image 5.29.2 \(marked as "1"\).

![](/assets/Img.5.29.2.jpg)

\[Image 5.29.2: Initializing the "button\_toggle" variable\]

When the board button is pressed, we need to toggle the current value of the button\__toggle variable_. There are a few way to go about doing this. An easy way is to simply multiply the current value of this variable by_ "_-1"_._ If it was \(-1\), then_ \(-1\) \* \(-1\) = 1_, and if it was "1" then _\(1\) \* \(-1\) = \(-1\)_.  _ _

In Image 5.29.3 you can see how to do this in your program.

![](/assets/Img.5.29.3.jpg)

\[Image 5.29.3: Inverting the status of the board button\]

This way, if the board button is pressed, then we set the opposite value to the "button\_toggle" by multiplying its current value by -1. You can find the "on board button" block in the "Robots" blocks group.

One last thing you need to do is to check the status of the on-board button \(stored in variable "button\_toggle"\) by using an "if...else" block, like you can see in Image 5.29.4.

![](/assets/Img.5.29.4.jpg)

\[Image 5.29.4: Checking the status of the board button\]

If the value of the variable is 1, the program will proceed with the functionality that you created previously that makes your mBot to follow the line.

If the value of the variable is -1, the program should simply stop the wheels from moving.

To implement this functionality, move all of the blocks from the previous chapter's program inside the "if" segment \(when the board button status is 1\), and add a block to stop the wheels \("move forward at speed 0"\) inside the "else" segment \(when the board button status is -1\)

You can see the current version of the program in Image 5.29.5. Go ahead and adjust your program to match the one in Image 5.29.5.

![](/assets/Img.5.29.5.jpg)

\[Image 5.29.5: The new modifications\]

Once you are finished with your modifications, upload it to your mBot. Now, every time you press the button, the wheels will either stop or start moving, depending on their last status.

That is the last bit of functionality that you add to the mBot for this course. But, there is still some housekeeping to do. Over the past few chapters, your program grew to a rather large size.

In the next chapter, you will learn how to break it down into smaller parts, called "functions". Breaking large programs into smaller functions make it easier to manage and improve. understand, and also reduces the risk of defects.

---

#### Question 5.29.1: What is the use of the on-board button?

A. It is meant by default to start and stop the wheels.

B. It starts and stops the power supply to the mBot.

C. It has a general use and it can be programmed to perform any programmed actions.

D. Both A and B.

_Answer: C_

---

**Question 5.29.2: Which of the following button conditions can be detected with the "on board button" block?**

A. Pressed

B. Toggle

C. Released

D. Tapped

_Answer: A and C_

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] You can start and stop your mBot by pressing its on-board button

\[   \] You know how to implement a toggle function with the on-board button

---



