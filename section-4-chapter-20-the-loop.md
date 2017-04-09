# Section 4

---

## Chapter 20: The loop

---

In this chapter you will learn about:

* How to use the forever loop
* How to save a program on the disk and load it again, when needed

---

Often we find ourselves in need of repetitive actions. A loop allows us to group together multiple instructions that we need to execute several times. To see such a loop in practice, let's create a new program that will make the two RGB LEDs blink in turns: the right LED will shine a particular colour, then it will go off, then the left LED will shine a different colour, then it will go off and then this process will repeat itself again, indefinitely.

We must know, by now, how to create a new program: File &gt; New and then, since we mean to program the mBot: "Robots" and place the "mBot Program" header onto the canvas.

### Looping "forever"

Loops are found in the yellow, "Control" group of instructions. We go there, pick the "forever" block and make it the first instruction just below the header block.

![](/assets/Img.4.20.1.jpg)

\[Image 4.20.1: The forever loop control instruction block\]

Whatever is placed within the forever block opening \(1\) is going to get repeated over and over again, forever, or at least until we either turn off the mBot or replace the program that is running with another program.

We have seen how to control the LEDs. Let's pick the correct blocks and edit their attributes to create the following program:

![](/assets/Img.4.20.2.jpg)

\[Image 4.20.2: The program for turning the LEDs on and off in turns\]

Reading the code: the left LED shines red for half a second, then it is turned off at the same time that the right LED starts to shine blue for another half a second, and then it is turned off. And that over and over again because it is contained in a "forever" loop.

If we connect the mBot and run the program we are going to see the two LEDs blink red and blue, in turns, very much like on a police patrol car.

### Changing the block order

Let's try a different approach now. For starters let's incorporate a variable in the program. That half a second that an LED is on can be stored in a variable. Let's create a new variable: Data&Blocks &gt; Make a Variable and give it the name "led\_on\_time", in the "New Varable" window. And then let's move the blocks around until we have the following program:

![](/assets/Img.4.20.3.jpg)

\[Image 4.20.3: The altered program\]

Let's try to read it, now. First of all we notice that there is a different organization of the instructions. At the same time that the left LED is turned on red, the right one is turned off and vice versa: when the right LED is turned on blue, the left one is turned off, which makes sense. Then we make use of a variable "led\_on\_time" that holds that half a second to wait, and we use this variable as attribute in the wait blocks, instead of the numerical.

Even though we have a different block order here, and an additional variable, we expect the program to execute the same way as before.

### Saving and Opening a program

We could take this one step further and use the proximity sensor on the mBot to change the amount of time that each LED is turned on, depending on the distance between the sensor and an object in front of it. For example, as the object goes closer to the mBot, the timing will be faster, and the object goes further away, the pace will slow down. We are going to see that in the next chapter and for that purpose we will be reusing the program that we created here. We need, therefore, to save it on the disk so that we can reload it later and extend it.

Saving a program on the disk allows us to reload it later on, eventually modify it, and re-execute it.

The way to save a program is by going to the file menu and either choose "Save Project" or "Save Project As". If this is the first time that we save a project then both options produce the same result: we will get the chance to pick a name for the program, and a location to save it.

As a general rule, we choose "Save Project as..." when we need to create a new copy of a saved program, either with a different name or in a different location. We use "Save Project" to just update the saved copy we are working on.

Let's save this one with the name "forever loop alternating the LEDs with variable".

Now imagine that we would like to share this code with a friend or a student, or to post it on the school website. In that case we can locate this file on the disk and attach it to an email or upload it to a web server.

To load a previously saved program we go to: File &gt; Load program and pick it in the "choose file to open" window. We might get a "Replace contents of current program?" question. If we are sure we have saved the program that is now on the canvas, or if we just don't need what's on the canvas, we can just proceed by clicking "OK".

### Questions

Question 4.20.1: When does the forever loop stop?

A. When we turn off the mBot

B. When we load a new program

C. When a wait block is executed

D. Both A and B

_Answer: D_

