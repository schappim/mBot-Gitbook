# Section 5

---

## Chapter 30: Custom blocks \(functions\)

---

In this chapter you will learn about:

* How to create a custom blocks \(a function\)
* How to give th
* How to use them in the program

---

At this point, in this mBot programming crash course, we have implemented all the functionality that we aimed for. The only problem is that we have ended up with quite a long program that is somehow both difficult to handle, when trying to order the instruction blocks, and also difficult to read, when we look at the instructions, trying to understand what the program does.

In this chapter we are going to see how we can simplify things by turning groups of instruction blocks into external functions that the main program can call by name.

The first thing to do is to have a look around the program and try to distinguish groups of blocks that implement a specific functionality. Let's take, for example, the two blocks that initialize the two variables "line\_sensor\_status" and "distance\_to\_obstacle":

![](/assets/Img.5.30.1.jpg)

\[Image 5.30.1: A likely candidate to become a function\]

These two instruction blocks can be seen as an entity and can, therefore, be turned into a single block or a function, like we use to call it. To do so we go to "Data&Blocks" \(1\) and there we click on "Make a Block" \(2\), like shown in the picture below:

![](/assets/Img.5.30.2.jpg)

\[Image 5.30.2: Where to create a new block \(a function\)\]

There will open a window where we can name our new block. Let's name it "read\_sensor\_data":

![](/assets/Img.5.30.3.jpg)

\[Image 5.30.3: The "New Block" window\]

and click "OK" once we have typed the name in the available text box. Notice how there is an "Options" button here. We we will see more of it later on.

There will appear a blue "define" block and we should move the two "set" variable blocks below it like this:

![](/assets/Img.5.30.4.jpg)

\[Image 5.30.4: The new "read\_sensor\_data" function\]

We notice there's a new block available, now, in "Data&Blocks", named "read\_sensor\_data". We can drag and drop it, like any other instruction block, and place it to be part of the program. Whenever reached by the program, this block will execute that smaller part of the program we placed aside: the new function shown in image 5.30.4.

We should place first in the forever block, replacing thus the two "set" variable blocks that we took away:![](/assets/Img.5.30.5.jpg)\[Image 5.30.5: Calling the new "read\_sensor\_data" function\]

Let's see if we can another group of instructions that implement together a specific functionality. Let's take, for example, the following group of instructions:

![](/assets/Img.5.30.6.jpg)

\[Image 5.30.6: Yet another candidate to become a function\]

This is a big chunk of blocks that can be described as doing one single thing: follow a line.

Following the same procedure, we can create a new block: Data&Blocks &gt; Make a Block and give the new block a suitable name, say "line\_follower".

This function will need to take input, though: the status of the line sensor. Therefore, in the "New Block" window, this time we do click on "Options" and then on "Add number input". This will create a new attribute next to the name of the block, where we can type a name for the input value. Let's type "line\_value" and when we have everything like shown in the image below, click "OK".

![](/assets/Img.5.30.7.jpg)

\[Image 5.30.7: Creating a new block that can take number input\]

Now, we should move that big group of blocks shown in image 5.30.6 and connect them below the new "define" block. In addition, we need to replace the "line\_sensor\_status", in the function, by the new input "line\_value". Just drug and drop it like shown in the image below:

![](/assets/Img.5.30.8.jpg)

\[Image 5.30.8: The new "line\_follower" function\]

Last step, we must call this new function, from within the program. In other words, we must place the new block in the "else", where the displaced group of blocks used to be, like shown in the image below:![](/assets/Img.5.30.9.jpg)

\[Image 5.30.9: Calling the new "line\_follower" function\]

But the function call is not ready yet. We need to make sure that the program will pass the status of the line sensor, stored in variable "line\_sensor\_status", to the function ![](/assets/Img.5.30.10.jpg)

\[Image 5.30.10: \]

Let's do one more and then I will leave the rest up to you to change as you see fit. Just experiment with this. The other part of the code that I would like to turn into a custom block, is the part where we implement the line following functionality. That code is right here, this bit. I'm going to create a new block, I’m going to call that Line Follower. I would like this to have a input now. I would like this to have the input and that input is the state of the sensor. The state of the sensor will be input to the Line Follower block. Let's call that Line Value. This allows us to create blocks that have parameters and then those parameters can be used inside the block just like any other variable.

I'm going to say okay, and here is the header for the new block. Then I will populate that block with the code inside here, inside this part of the if/else statement. This is where we have a line following code. We're going to drag that over and put it here. Of course, I need to be able to call the Line Follower block. To do that, I'm going to drag the Line Follower block and put it where this bit of code used to be. Remember that we need a parameter here and the parameter that I want to pass is the Line Value, so the value that the line sensor has returned. I need to grab that line sensor status and put it in here.

Because now inside our block we have replaced the original line sensor status with a local variable line value, which eventually contains the same value but it's got a different name. One, Line Value is the internal name that is used inside the block, while line sensor status belongs to the outside program to the whole program. Just going to move that Line Value variable and replace any reference of the original line sensor status. Just like that. Okay, so this is what our new program looks like. If you look around the original program, there are still things that you can do to simplify it and convert some of its components into external blocks, custom blocks.

I think it's good enough for now. I’d like to upload that and make sure that my robot still works. Plug it into the USB. Actually, I don't need to turn it upside down because I've got the button functionality. Connect to comp six. Right click on the input header and upload to Arduino, and upload to Arduino, all done. Let's see, does it still work? I'm going to press the button, it looks like it is. All right. Let's go and try it out then on the track and hopefully everything would go well. The input now contains the last version of the program. It's supposed to behave in the exact same way as the previous version, it's just that now it's more organized using custom blocks than just having a one monolithic piece of code.

Let's start it and see how it behaves. Yes, it looks like it behaves exactly like it did before. Great, okay, that's it. At this point, we've got the mBot behaving in the way that we planned for. It can follow a line, it can turn around when it reaches the end of the line and detects the obstacle in front of it. We were also able to improve the construction of our program by using custom blocks. Let's wrap it up in the next lecture and discuss things that your students can actually do going forward.

