# Section 3

---

## Chapter 17: Moving left, right, backwards

---

In this chapter you will learn about:

* How to make the mBot turn left and right
* How to make the mBot go backwards
* What is a variable and how to use it
* How to use an arithmetic operand

---

**This chapter contains hand-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will compose a sketch that makes your mBot turn left and right.

---

In the last chapter you programmed the mBot to move forwards for five seconds at speed 125 and then stop.

In this chapter you will continue working on the same program and add to the ability to turn left or right, and also move backwards.

### Turn left, right and go backwards

In order to make the mBot turn, you are going to change the direction attribute of the last instruction block. Just click on "run forward" and pick "turn right" from the drop-down menu.

![](/assets/Img.3.17.1.jpg)

\[Image 2.17.1: Altering the direction attribute\]

Don't forget to set some speed, of course, other than zero. Click on the speed attribute and pick 100 from the drop-down menu. Then go on and compose the following program, dragging and dropping blocks and setting their attributes:

![](/assets/Img.3.17.2.jpg)

\[Image 2.17.2: A program with all kinds of wheel motion\]

The "wait" blocks maintain the previous instruction for one second, before moving to the next one.

---

#### Question 3.17.1: The very last "run forward" instruction has its speed parameter set to zero. What will the mBot do when it reaches this instruction?

A. It will continue moving forwards at the previously set speed.

B. It will stop.

C. It will reverse

D. It will blink its RGB LEDs

_Answer: B_

---

#### DID YOU KNOW?

Even though not as fast as the processor of your computer, the processor inside the mBot is fairly fast. It operates at 16 megahertz, which means that it can execute 16 million instructions every single second! Isn't that impressive?

---

After you are done, connect the USB cable on the mBot, connect to the COM port, right-click and "Upload to Arduino" and see the mBot move following the instructions.

### Introducing a variable

Let's look at a new programming concept, now: the variable.

Looking at the program we notice that we've got a speed of 100 in four of the move blocks. If you would like, for some reason, to change the speed to 150, you would have to individually change that in all the movement blocks. Imagine a program with dozens of such instructions that need to be adjusted. To avoid such a tedious job, you can use a variable. A variable is like a storage area that can contain a value: some text or some number.

Back to our program, you can create a variable to store a number that represents a speed. To do that go to Scripts &gt; Data&Blocks &gt; Make a Variable \(see Image 2.17.3\).

![](/assets/Img.3.17.3.jpg)

\[Image 2.17.3: Creating a variable\]

In the window that opens you can type a name for the variable. Variable names need to be descriptive of the values they are going to hold. You need the variable to store a value for the speed of the wheels so an obvious choice would be "wheel\_speed". You can use the underscore to connect multiple words because spaces are not allowed in variable names.

![](/assets/Img.3.17.4.jpg)

\[Image 2.17.4: Giving a name to the variable\]

Scratch programs often uses "Sprites" as the object on which a program operates, but we use the mBot instead. So just ignore the two radio buttons under the "Variable name" text field, titles "For all sprites" and "For this sprite only". Just click "OK" to close this dialog box.

After that, you have a brand new variable available, that is, some storage space with the reference name "wheel\_speed". You will notice that after creating the variable, new instruction blocks appear in the "Data&Blocks" segment.

Now, you first need to store some number in your new variable and then use it within the instruction blocks. To store a value in the variable you need the "set..." block.

![](/assets/Img.3.17.5.jpg)

\[Image 2.17.5: The variable blocks\]

Drag and drop it onto the canvas, attaching it immediately after the header block \(1\), and then set the value attribute to some speed, say 150. From now on, you can use the variable name instead of the numeral 150. You can do that by picking the "wheel\_speed" variable block and drag and drop it into the speed attribute of each move block \(2\). ![](/assets/Img.3.17.6.jpg)\[Image 2.17.6: Using the variable in the program\]

### Introducing an arithmetic operand

Let's add a little twist. Let's say that for the first "run forward block", instead of 150 you want a speed of 125 and here's a way to handle it. Go to "Operators" \(the green family of blocks\) and drag and drop the second operator block, the one with the minus, onto the canvas. The minus operator takes two operands, one on each side. Drag and drop the variable block "wheel\_speed" and make it the first operand and then type 25 as the second one. When you are done you can drag and drop the whole block it into the "run forward" block, so that the whole expression "wheel\_speed - 25" becomes the new speed attribute, like in the image below.

![](/assets/Img.3.17.7.jpg)

\[Image 2.17.7: Subtracting 25 from the wheel\_speed variable\]

Once you are have that you can run the new program:

![](/assets/Img.3.17.8.jpg)

\[Image 2.17.8: The final program\]

Make sure the USB cable is connected and we are connected to a COM port and then "Upload to Arduino".

### Questions

Question 3.15.1: How can you make the mBot turn left?

A. You use a combination of three different move blocks.

B. You use a move block and set the first attribute to "turn left".

C. You use a move block and set the second attribute to "turn left".

D. You use a "turn right" block with a negative speed value.

_Answer: B_

Question 3.17.2: How can you best describe a variable?

A. As an arithmetic expression.

B. As a value.

C. As storage space.

D. As an operation between two operands.

_Answer: C_

