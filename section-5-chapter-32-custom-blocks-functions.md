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

But the function call is not ready yet. We need to make sure that the program will pass the status of the line sensor, stored in variable "line\_sensor\_status", as an attribute to the function. To achieve that, we need to take the "line\_sensor\_status" variable block and drag and drop it in the "line\_follower" block \(1\) as an attribute: ![](/assets/Img.5.30.10.jpg)\[Image 5.30.10: passing and attribute to the function\]

Now, when we run the program and the execution reaches the "line\_follower" block, the program will call function "line\_follower" passing it the value of variable "line\_sensor\_status" \(2\). What will happen is that the value of "line\_sensor\_status" will be copied to local variable "line\_value", in order to be used by the function according to its needs. 

"line\_sensor\_status" belongs to the main program when "line\_value" is used locally by function "line\_follower".

We can check the program for more things that can be turned into functions, simplifying the main program, but instead we will "Upload to Arduino" and check if the program executes like before, making sure we didn't mess our program while creating functions.

Functions help organizing programs better by breaking them down in smaller parts, instead of building one monolithic program that is both difficult to read and understand what it does, and to edit.

The mBot has preserved all the functionality we aimed for: it can follow a line, it can detect an obstacle and make a U-turn. Only now our program is better organized, too. The instructions are more readable.

Let's wrap it up in the next lecture and discuss things that your students can actually do, going forward.

### Exercise



