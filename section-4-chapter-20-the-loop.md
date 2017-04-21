# Section 4

---

## Chapter 20: The loop

---

**In this chapter you will learn about:**

* How to use the forever loop
* How to save a program on the disk and load it again, when needed

---

**This chapter contains hands-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will compose a sketch that makes use of loops to repeat a segment of code, and learn about to save your program.

---

Often, you will encounter the need to have your program execute several instructions many times. In such cases, you can use the loop programming structure. There are several variations of the loop structure, but in this chapter you will learn about the simplest one which you can use to repeat a set of instructions for ever \(or, at least, until you turn off your mBot, reset it, or upload a new program\).

To see such a loop in practice, let's create a new program that will make the two RGB LEDs blink in a specific pattern:

1. the right LED will turn on in a particular colour, 
2. then it will turn off, 
3. then the left LED will turn on to a different colour, 
4. then it will turn off and 
5. then this process will repeat itself again, indefinitely.

You should know, by now, how to create a new program: In the mBlock menu, select File &gt; New and then, since we mean to program the mBot: "Robots" and place the "mBot Program" header onto the canvas.

### Looping "forever"

Loops are found in the yellow, "Control" group of instructions. Go there, pick the "forever" block and make it the first instruction just below the header block.

![](/assets/2017-04-13_12-23-31.png)

\[Image 4.20.1: The forever loop control instruction block\]

Any Scratch blocks bound within the forever block will be repeated over and over, forever, or at least until we either turn off the mBot or replace the program that is running with another program.

You have learned how to control the onboard LEDs. Go ahead and drag the appropriate blocks to compose the following program \(see Image 4.20.2\):

![](/assets/Img.4.20.2.jpg)

\[Image 4.20.2: The program for turning the LEDs on and off in turns\]

Let's read the program inside the "forever" loop, one block at a time:

1. Turn the left LED light up in red for half a second,
2. then, turned the left LED off and at the same time turn the right LED light up in blue for another half a second,
3. then, turned the right LED off. 
4. After that, the loop will back to its beginning and the same code will execute again.

Go ahead, connect your mBot to your computer and upload the program. You will see the two LEDs blinking red and blue, in turns, very much like on a police patrol car.

### Add a variable

Let's try a different approach now. Let's start by adding a variable to the program. You can use the new variable to store the amount of time for which the LEDs should stay on. This way, you will be able to change this duration at one place only in your program, instead of doing multiple changes throughout it.

In the previous version of the program, you specified that the LEDs should be on for 0.5 seconds, by typing "0.5" in the "wait" blocks. This value of "0.5" can be stored, instead, in a variable.

Go ahead and create a new variable \(refer to chapter 17 if you don't remember how to do this\): _Data&Blocks &gt; Make a Variable_ and give it the name "led\_on\_time", in the "New Variable" window.

Adjust your program so that you reach this new version:

![](/assets/Img.4.20.3.jpg)

\[Image 4.20.3: The altered program\]

Read it line by line to understand the changes.

First, notice that we have changed the sequence and organisation of the blocks. The result of this is a program that is easier to read. For example, at the top of the "forever" loop, you can see that there are two blocks that control the LEDs. The first one, makes the left LED turn on in red, and the second block turn off the right LED. In other words, at the same time that the left LED is turned on red, the right one is turned off.

Then, there is a "wait" block, which keeps the left LED on for 0.5 seconds \(this value is stored in the "led\_\_on\_\_time" variable\).

After than, the left LED is turned off and the right LED is turned on to blue.

There's another "wait" block, keeping the left LED off and the right LED blue for 0.5 seconds, before these 6 blocks are executed again.

Even though we have a different block order here, and an additional variable, we expect the program to execute the same way as before. There are many ways to write a program that does the same thing, but as the programmer, you should try create programs that are easy to read, clear and concise.

---

**Question 4.20.1: Change your existing program so that the left and right RGB LEDs turn on for different amounts of time. Make the left LED stay on for 0.5 seconds, and the right LED stay on for 0.3 seconds. Use variables to store these durations.**

_Answer: Here's an example program that answers this question_

![](/assets/2017-04-22_08-04-48.png)

---

#### Question 4.20.2: You can control the amount of time that the LEDs stay on by using input from the proximity sensor, instead of using a fixed value in a variable. You can make the LEDs stay on depending on the distance between the sensor and an object in front of it. As the object goes closer to the mBot, the timing will be faster, and the object goes further away, the pace will slow down. Modify your existing program to accordingly to achieve this objective.

_Answer: Here's an example program that answers this question_

![](/assets/2017-04-22_08-11-00.png)

---

## Saving and Opening a program

Saving a program on the disk allows you to reload it later on, eventually modify it, and re-execute it.

The way to save a program is by going to the file menu and either choose "Save Project" or "Save Project As". If this is the first time that you save a project then both options produce the same result: you will get the chance to pick a name for the program, and a location to save it.

As a general rule, choose "Save Project as..." when you need to create a new copy of a saved program, either with a different name or in a different location. Use "Save Project" to just update the saved copy you are working on.

Let's save this one with the name "forever loop alternating the LEDs with variable" \(see Image 4.20.4\).

![](/assets/file save.png)

\[Image 4.20.4: Saving a program to your computer\]

Now imagine that you would like to share this code with a friend or a student, or to post it on the school website. In that case you can locate this file on the disk and attach it to an email or upload it to a web server \(see Image 4.20.5\).

![](/assets/2017-04-22_08-19-02.png)

\[Image 4.20.5: This file \(ending in "sb2"\) contains your mBot program, stored on your computer\]

To load a previously saved program you go to: File &gt; Load program and pick it in the "choose file to open" window. You might get a "Replace contents of current program?" question. If you are sure you have saved the program that is now on the canvas, or if you just don't need what's on the canvas, you can just proceed by clicking "OK".

---

### **Question 4.20.3: When does the forever loop stop?**

A. When you turn off the mBot

B. When you load a new program

C. When a wait block is executed

D. Both A and B

_Answer: D_

---

Question 4.20.4: Is it possible to share your mBot programs with others?

A. Yes

B. No

_Answer: A_

---

**Question 4.20.5: What is the process you must follow if you want to share your mBot program with a friend?**

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

_Answer: Save your program to your computer, locate the file \(ending in ".sb2"\), then email it to your friend, use a USB drive , or transfer it via the network._

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] You know how use the loop structure

\[   \] You know how to use variables to store values

\[   \] You know how to use a value stored in a variable

\[   \] You know how to store a reading from a sensor in a variable

\[   \] You know how to save your program to your computer

\[   \] You know how to load your program stored on your computer in mBlock for editing

\[   \] You know how to share your program with other people

