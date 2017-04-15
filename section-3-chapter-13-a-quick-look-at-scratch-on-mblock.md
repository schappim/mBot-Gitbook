# Section 3

---

## Chapter 14: A quick look at Scratch

---

**In this chapter you will learn about:**

* What are the basic blocks for creating a Scratch program
* How to control the movement of a sprite
* How to print messages from a Scratch program
* How to execute a program
* How to add and remove blocks to and from a program
* How to repeat a segment of your program many times

---

**This chapter contains hand-on activities.**

You will not need any tools.

You will need mBlock installed on your computer. In this chapter you will only compose programs that control the Panda Sprite in the Stage area. You will not need your mBot, so you may put it aside for now.

---

Now that you have installed mBlock on your computer, go ahead and start it, if you have not already done so.

In this chapter you will not play with the mBot. Instead, you will learn how to manipulate the movement of the Panda sprite by writing a simple Scratch program. As you do that, you will learn how to use some of the most common Scratch programming blocks.

![](/assets/2017-03-24_16-46-55.png)

\[Image 14.1: In this chapter you will learn how to control the Panda using Scratch\]

Let's start with the "Say" block.

![](/assets/2017-03-24_16-50-35.png)

\[Image 14.2: The "Say" block\]

The "Say" block allows you to print a text message in a bubble over the Panda. Select the Scripts tab from the blocks palette, and find the "Say" block at the top of the Looks group of blocks. Click on it, and while you hold the mouse button, drag the block into the Script area.

By default, this block simply prints "Hello" over the Panda, but you can change this text to anything you like. Simply click on the white text box and replace the current text with something else. Write "Hello world," for example, by clicking in the text box marked "1" in Image 14.3. You can also control how long you'd like the message to appear for, before it disappears. Let's make it two seconds by clicking in the text box marked "2" in Image 14.3.

![](/assets/2017-03-24_16-58-03.png)

\[Image 14.3: The "Say" block has two attributes that you can change, the Text and the Duration attributes\]

Now you have a block that is meant to show the text "Hello World!" for two seconds next to the Panda sprite. This is a program, with only one block of code in it. But how do you actually trigger \(start\) the program, so that it actually does what you designed it to do?

You need to use another block, the purpose of which is to start the execution of a program. There are a few such blocks, under the Event group of blocks, inside the Scripts tab of the Blocks palette \(see Image 14.4\).

![](/assets/2017-03-25_09-33-18.png)

\[Image 14.4: Get the trigger block from the Events group in the Scripts tab\]

Find the block with the green flag in it, drag it \(by clicking on it and holding the mouse button down\), over the existing "Say" block in the Script area. As you move the Green flag block over the "Say" block, you will notice that a white outline appears. This indicates that the two blocks can work together. Not all blocks are compatible with each other. The white outline is a confirmation that they are compatible. You can let go of the button, and then two blocks will snap together, and connect.

![](/assets/2017-03-25_09-40-24.png)

\[Image 14.5: Click on the Green flag icon to start your program\]

Now, click on the Green flag icon at the top right side of the Sprite area. This will start the program that is connected to the Green flag block.

In Image 14.6 you can see how the text that you typed in the "Say" block appears inside a bubble over the Panda sprite for two seconds, and then disappears.

![](/assets/2017-03-25_10-04-29.png)

\[Image 3.14.6: The text message appears in a bubble, next to the Panda\]

Congratulations! You just executed your first Scratch program!

---

**Exercise 14.1: **Now that you know how to get your Panda Sprite to talk, how about you get it to "say" a couple of sentences?

Compose a small program that makes the Panda say something like this:

* Sentence 1: "Hello, I am Panda".
* Sentence 2: "What is your name?"
* Sentence 3: "Good to meet you Peter!"

Of course, replace "Peter" for your own name. And design your program so that there are appropriate delays for the first two sentences. But, compose your program so that the last sentence is "said" permanently, that is, so that it does not disappear after an amount of time.

_Answer:_

![](/assets/2017-04-06_17-14-48.png)

---

In the Events group of blocks, there are several other triggers that you can use in your programs. For example, you may want to get the Sprite to move or to "Say" something when you press a key on your keyboard, instead of clicking on the Green icon. To do this, you can use the "When key pressed" block. In Image 14.7, you can see a variation of the program you wrote earlier.

![](/assets/2017-03-25_10-08-42.png)

\[Image 14.7: Use a different trigger to get the Panda to speak\]

Let's modify the existing program so that the Panda speaks when you press the space bar on your keyboard. First, detach the "Say" block from the Green flag block, and move it somewhere else in the Script area. Then, drag the "When space key pressed" block over the "Say" block, and lock it in place. Notice that if you click on the text box that currently contains the word "space", you will be able to select one of several other keys, instead of space. Select one of them, or just leave the currently selected "space" as your desired key. Now, press the space bar on your keyboard. Notice that "Hello world" appeared again in a bubble over the Panda, just like in the first program.

So, what you have learned so far is that in order to start a program you need a trigger. You can have more than one program in your Scripts area, and as long as each one of them has a trigger at the top, you will be able to start them.

---

**Exercise 14.2: **Try this: Create three programs with appropriate triggers. Design your programs so that when you press the key "A" on your keyboard, the Panda will say "you pressed A". Similarly, your Panda will say "you pressed B", and "you pressed C" when you press "B" and "C" respectively.

Answer:

![](/assets/2017-04-06_17-18-59.png)

---

Now let's do something else. Detach the "Say" block from the "When" block and then delete the "When" block. There are two ways to delete a block. First, you can right-click on it and select "Delete" from the submenu that appears \(Image 14.8\). You can also drag the block inside the Blocks palette.

![](/assets/2017-03-25_10-19-20.png)

\[Image 14.8: Deleting a block by right-clicking on it and selecting "delete"\]

![](/assets/2017-03-25_10-19-45.png)

\[Image 14.9: Deleting a block by dragging it to the Blocks Palette \(where it came from\)\]

Next, let's make the Panda move.

Select the Motion group. All the block in that group can produce some kind of movement.

![](/assets/2017-03-25_10-24-13.png)

\[Image 14.10: The blocks inside the Motion group\]

Drag the Move block \(at the very top of the group\) and connect it to the Green flag trigger in the Script area. Click inside the text box of the Move block and change the value from "10" to "50". This value controls how far the Panda will move. Each step is tiny, so using the value "50" will cause the Panda to move further away from its starting point, and will make it easier to see the movement. Then, connect the "Say" block to the end of the program. The objective is to make the Panda move by 50 steps, and when it finishes, to say "Hello World!" for two seconds.

![](/assets/2017-03-25_10-24-54.png)

\[Image 14.11: This program makes the Panda move and speak\]

Before you click on the Green flag, click on the Panda and drag it a bit to the left edge of the Sprite area. This will leave more available space to its right to move. OK, now click on the Green flag. See what happened?

![](/assets/2017-03-25_10-31-59.png)

\[Image 14.12: The Panda moves 50 steps and then speaks!\]

---

**Exercise 14.3: **Make Panda to do something more elaborate. Get it to move by 50 steps, then to turn by 45 degrees, then to move by another 50 steps, and then make it say, "Hello World!".

_Answer:_

![](/assets/2017-03-25_10-35-14.png)

\[Image 14.13: This program makes the Panda move straight, turn, and speak\]

---

The program from question 14.3 will cause the Panda to move so fast that as soon as you click on the Green flag, the whole program will be complete. To slow it down, you can use the "wait" block. Select the Control group of blocks, and drag two "wait" blocks, one before the "turn" block and one after the "turn block. You can see the new program in Image 14.13.

![](/assets/2017-03-25_10-38-16.png)

\[Image 14.14: Using the "wait" block\]

Change the wait time to 2 seconds \(instead of 1 second\), and click on the Green flag. You will see the Panda moving 50 steps, then waiting for 2 seconds, then turning by 45 degrees, then waiting for 2 seconds, then moving for another 50 steps and finally speaking to us.

The parameter of the "wait" block can be a whole number or a decimal, like 0.5 seconds.

You can edit the parameters of a sprite by clicking on the "i" button at the top left corner of the sprite's icon \(see Image14.15\).

![](/assets/2017-03-25_11-10-20.png)

\[Image 14.15: Editing the parameters of a sprite\]

When you are in sprite edit mode, you can change the name of the sprite, you can call it mBot, for example, or mBot Panda to be more specific. You can also change its direction by manipulating the direction knob. Go ahead, use these controls to change the name of your sprite to "M-Bot-Panda", and its direction to 90 degrees.

![](/assets/2017-03-25_11-13-44.png)

\[Image 14.16: Editing the parameters of a sprite\]

Next, let's try out one of the available control structures. In particular, I would like to use a control structure that allows us to execute a block of code many times. Please follow along with this example.

Select the Control group from the Scripts tab, and drag the "Repeat" block into the Scripts area. Arrange the program as is shown in Image 14.17.

![](/assets/2017-03-25_11-19-12.png)

\[Image 14.17: Insert the "Repeat" block\]

Notice that the "Repeat" block is shaped so that it encloses other blocks. It takes a single parameter, which is the number of times that we would like to repeat the code that it contains. In the case of the example, it is 10 times, but you can change that to whichever value you like. I'd like the sprite to say "Hello World!" when the 10 repeats are complete, so drag the "Say" block at the end of the "Repeat" block and change the default text. Image 14.17 shows the program at this point \(the parameter for the "Wait" block is now 1 second to make the sprite move a bit faster\).

![](/assets/2017-03-25_11-24-58.png)

\[Image 14.18: The current version of the program\]

There are a lot more blocks which you can play around with, so I invite you to experiment with those programming blocks and get your sprite to do different things like move and a box path, or around a circle or move. You can also get it to say things depending on its location, for example. Or you can program it to produce sounds. Experiment with the sound blocks for this kind of outcome.

---

**Exercise 14.4: **Have a look in the Pen block category, in the Blocks Palette. Notice that this category contains blocks that you can use to draw shapes in the Stage area. Once you attach a pen to the Panda, the pen will leave a trace behind the Panda as the Panda moves.

Compose a program that uses the Pen block so that it draws a box when you press the "d" key on your keyboard.

_Answer:_

![](/assets/2017-04-06_17-37-10.png)

Notice: of course, instead of using a negative turn angle you could use the anticlock-wise turn block, with a positive angle.

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] You know how to move the Panda Sprite in a straight line

\[   \] You know how to make the Panda Sprite turn

\[   \] You know how to make the Panda Sprite speak

\[   \] You know how to trigger a program via the keyboard

\[   \] You know how to trigger a program by clicking on the green flag

\[   \] You know how to repeat a segment of your program for a specific number of times

