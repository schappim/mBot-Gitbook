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

In the last chapter we programmed the mBot to move forwards for five seconds at speed 125 and then stop.

In this chapter we will continue building on the same program and we will add to the mBot the ability to turn as well, either left or right, and also move backwards.

### Turn left, right and go backwards

In order to make the mBot turn, we are going to change the direction attribute of the last instruction block. Just click on "run forward" and pick "turn right" from the drop-down menu.

![](/assets/Img.3.17.1.jpg)

\[Image 2.17.1: Altering the direction attribute\]

We shouldn't forget to set some speed, of course, other than zero. Let's click on the speed attribute and pick 100 from the drop-down menu. And then let's go on and build the following program, dragging and dropping blocks and changing their attributes:

![](/assets/Img.3.17.2.jpg)

\[Image 2.17.2: A program with all kinds of wheel motion\]

The wait blocks take care that the mBot changes smoothly from one move to the other. The last one, at speed zero, just stops the spinning.

**Note**: Even though not as fast as the subprocessor of general purpose computer, the processor inside the mBot is fairly fast. It operates at 16 megahertz, which means that there's clock that ticks 16 million times per second and that's how many instructions it can execute. Its quite a lot!

After we are done, we connect the USB cable on the mBot, we connect to the COM port, we right-click, "Upload to Arduino" and see the mBot move following the instruction blocks.

### Introducing a variable

Let's look at a new programming concept, now: the variable.

Looking at the program we notice that we've got a speed of 100 in four of the move blocks. If we would like, for some reason, to change the speed to 150, we would have to individually change that in all the move blocks. Imagine a program with dozens of such instructions than need to be adjusted.

To avoid such a tedious job, we can use a variable. A variable is like a storage area that can contain a value: some text or some number.

Back to our program, we need to store a number.

The first step is to create a variable. To do that we go to Scripts &gt; Data&Blocks &gt; Make a Variable

![](/assets/Img.3.17.3.jpg)

\[Image 2.17.3: Where to create a variable\]

In the window that opens we can choose a name for the variable. Variable names need to be descriptive of the values the are going to hold. We need the variable to store a value for the speed of the wheels so an obvious choice would be "wheel\_speed". We use the underscore to connect multiple words because spaces are not allowed in variable names.

![](/assets/Img.3.17.4.jpg)

\[Image 2.17.4: Giving a name to the variable\]

Scratch often uses "sprites" but we use the mBot instead so we shouldn't worry much about the two sprite connected options, found here, and just leave the default option "For all sprites" set, and click on "OK".

After that, we have a brand new variable available, that is some storage space with the reference name "wheel\_speed". We will notice that after creating the variable, new instruction blocks appear in the "Data&Blocks" segment.

Now, we need first to store some number in our new variable and then use it within the instruction blocks. To store a value in the variable we need the "set..." block.

![](/assets/Img.3.17.5.jpg)

\[Image 2.17.5: The variable blocks\]

We drag and drop it onto the canvas, immediately after the header block \(1\), and then we set the value attribute to some speed, say 150. From now on, we can use the variable name instead of the numeral 150. We can do that by picking the "wheel\_speed" variable block and drag and drop it into the speed attribute of each move block \(2\). ![](/assets/Img.3.17.6.jpg)\[Image 2.17.6: Using the variable in the program\]

### Introducing an arithmetic operand

Let's add a little twist. Let's say that in the first "run forward block", instead of 150 we want a speed of 125 and here's a way to handle it. We go to "Operators" \(the green family of blocks\) and drag and drop the second operator block, that with the minus, onto the canvas. The minus operator takes two operands, one on each side. We drag and drop the variable block "wheel\_speed" and make it the first operand and then type 25 as the second one. When we are done we can drag and drop it into the "run forward" block, so that whole expression "wheel\_speed - 25" becomes the new speed attribute like in the image below.

![](/assets/Img.3.17.7.jpg)

\[Image 2.17.7: Subtracting 25 from the wheel\_speed variable\]

Once we've done that we can run the new program:

![](/assets/Img.3.17.8.jpg)

\[Image 2.17.8: The final program\]

We make sure the USB cable is connected and we are connected to a COM port and then "Upload to Arduino".

### Questions

1.How can we make the mBot turn left?

A. We use a combination of three different move blocks

**B. We use a move block and check the first attribute to "turn left"**

C. We use a move block and check the second attribute to "turn left"

D. We use a "turn right" block with a negative speed value

2.How can we describe a variable?

A. As an arithmetic expression

B. As a value

**C. As storage space**

D. As an operation between two operands

