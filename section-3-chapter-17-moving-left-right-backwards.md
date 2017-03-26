# Section 3

---

## Chapter 17: Moving left, right, backwards

---

In this chapter you will learn:

* How to make the mBot turn left and right
* How to make the mBot go backwards
* What is a varialbe and how to use it

---

In the last chapter we programed the mBot to move forwards for five seconds at speed 125 and then stop.

In this chapter we will continue building on the same program and we will add to the mBot the ability to turn as well, either left or right, and also move backwards.

In order to make the mBot turn, we are going to change the direction attribute of the last instruction block. Just click on "run forward" and pick "turn right" from the drop-down menu.

![](/assets/Img.3.17.1.jpg)

\[Image 2.17.1: Alterning the direction attribute\]

We shouldn't forget to set some speed, of course, other than zero. Let's click on the speed attribute and pick 100 from the drop-down menu. And then let's go on and build the following program, dragging and dropping blocks and changing their attributes:

![](/assets/Img.3.17.2.jpg)

\[Image 2.17.2: A program with all kinds of wheel motion\]

The wait blocks take care that the mBot changes smoothly from one move to the other. The last one, at speed zero, just stops the spinning.

**Note**: Even though not as fast as the subprocessor of general purpose computer, the processor inside the mBot is fairly fast. It operates at 16 megahertz, which means that there's clock that ticks 16 million times per second and that's how many instructions it can execute. Its quite a lot!

After we are done, we connect the USB cable on the mBot, we connect to the COM port, we right-click, "Upload to Arduino" and see the mBot move following the instruction blocks.

### Variables

Let's look at a new programming concept, now: the variable.

Looking at the program we notice that we've got a speed of 100 in four of the move blocks. If we would like, for some reason, to change the speed to 150, we would have to individually change that in all the move blocks. Imagine a program with dozens of such instructions than need to be adjusted.

To avoid such a tedious job, we can use a variable. A variable is like a storage area that can contain a value: some text or some number.

Back to our program, we need to store a number.

The first step is to create a variable. To do that we go to Scripts &gt; Data&Blocks &gt; Make a Variable

![](/assets/Img.3.17.3.jpg)

\[Image 2.17.3: Where to create a variable\]

In the window that opens we can choose a name for the variable. Variable names need to be descriptive of the values the are going to hold. We need the variable to store a value for the speed of the wheels so an obvious choise would be "wheel\_speed". We use the underscore to connect multiple words because spaces are not allowed in variable names.

![](/assets/Img.3.17.4.jpg)

\[Image 2.17.4: Giving a name to the variable\]

Scratch often uses "sprites" but we use the mBot instead so we shouldn't worry much about the two sprite connected options, found here, and just leave the default option "For all sprites" set, and click on "OK".

After that, we have a brand new variable availabe, that is some storage space with the reference name "wheel\_speed". We will notice that after creating the variable, new instruction blocks appear in the "Data&Blocks" segment.

Now, we need first to store some number in our new variable and then use it within the instruction blocks. To store a value in the variable we need the "set..." block.

![](/assets/Img.3.17.5.jpg)

\[Image 2.17.5: The variable blocks\]

We drag and drop it onto the canvas, immediately after the header block \(1\), and then we set the value attribute to some speed, say 150. From now on, we can use the variable name instead of the numeral 150. We can do that by picking the "wheel\_speed" variable block and drag and drop it into the speed attribute of each move block \(2\). ![](/assets/Img.3.17.6.jpg)\[Image 2.17.6: Using the variable in the program\]

Let's add a little twist. Let's say that in the first "run forward block", instead of 150 we want a speed of 125 and here's a way to handle it. We go to "Operators" \(the green family of blocks\) and drag and drop the second operator block, that with the minus, onto the canvas. The minus operator takes two operands, one on each side. We drag and drop the variable block "wheel\_speed" and make it the first operand and then type 25 as the second one. When we are done we can drag and drop it into the "run forward" block, so that whole expression "wheel\_speed - 25" becomes the new speed attribute like in the image below.

![](/assets/Img.3.17.7.jpg)

\[Image 2.17.7: Subtracting 25 from the wheel\_speed variable\]

**{up to here edited by Dimitris}**

~~~~~~~~~

The two options down here for all sprite or for this sprite only basically say that this variable will be available to all your programs but don't worry about it because we're not using sprites anyway, we're using the mBot. Just accept the default for all sprites and hit okay. Now, we've got the wheel speed variable. In order to interact with these variable, we have access to a number of new blocks.

We want to set the wheel speed value to a particular number. To do that, we've got this block here. I'm going to drive this block and put it up here, the beginning of the program which is a reasonable place to set a new variable. You can set a variable to a number such as, as I said earlier, let's make it a 150. This is going to make a robot go quite a bit faster than it previously did.

You can also get values into your valuable from things like senses. Again, this is something that I'm going to show you later but for now let's just hard code this speed into the wheel speed variable using the set block. The next thing to do is, to update or to change the movement blocks so that instead of a fixed speed, we set it to the that is stored inside the wheel speed variable. To do that, we simply get the variable from the data and block section and move it across into the program. Put the left side of the wheel speed variable block, so that it can attach this on the textbooks. We can see that it highlights and when it highlight it means that you can then let go of your mouse and then the variable gets inserted into the text area. I can do that for the rest of the text areas. I like that. I'm going to leave the last one as zero because I want my robot eventually to stop.

While I’m at this, I'd like to show you one more trick. Let's say that I would also like to use the same variable to provide a speed value for the first run forwards block. The problem here is, you can see that right now I've got 125 which is not the same value as what I've got now stored in wheel speed. The run forward speed for the first block is 25 units smaller than the 150 value that I’ve stored in the wheel speed variable. What this means, is that I need a way to do a simple calculation like a subtraction.

I would like, for example, the speed by which the m-word moves forwards -- the first time that one as soon as I turned on to be 25 units smaller than the speed that I've stored in the wheel speed variable. It means that I need to use an operator. I'm going to go to the operator’s section. You can see that I've got a bunch of operators here. I’m going to talk about some of those later. But for now, I want to show you subtraction.

Here is a subtraction, you also have addition, multiplication and division. I can use that in order to achieve my objective here. There is my subtraction. I want to take my wheel speed, speed value, whatever I’ve stored inside this variable and subtract 25 from it like that. I'm going to take this block and use it to replace the fixed speed 125 in my first speed of movement block. Okay, that looks like it's complete. This is what I want to achieve for this iteration of the program. You can see that my program, the Arduino version has been updated. I've got my variable here, wheel speed 150. I’ve got the first movement instruction, which says whatever wheel speed you've set in this variable, subtract 25 from it. That then becomes the speed for both wheels and when the Arduino turns on.

Okay, let's upload the sketch. Plug in the USB cable to the Arduino. I’m going to turn it upside down so it doesn't fly off my table. Okay. Let's upload the sketch to the Arduino. Uploading. You can notice that the wheels are now spinning faster than before this, because now we've got the speed 150. See how easy it is to change the speed for all of the movements, for all the individual movements by just changing a single variable. Let's change that top speed. Let's make it 255 and see how fast that goes. Upload. That's the maximum speed 255. Great, that's what variables are useful for. I’m going to turn that down to maybe a 125. More reasonable speed for the amount of real estate that I have on the floor to work with and leave it at that.

Okay, great. I think at this point you are starting to get a good understanding of how movement can be achieved with the mBot. The next part of this crash course, I would like to talk about a very important programming concept that is the loop. We'll use the loops to do some interesting visual effects with the RGB LEDs.

