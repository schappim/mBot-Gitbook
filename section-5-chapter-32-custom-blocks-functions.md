# Section 5

---

## Chapter 30: Custom blocks \(functions\)

---

In this chapter you will learn about:

* How to create a custom blocks
* When to create a custom block
* How to pass values to a a custom block as attributes

---

At this point, in this mBot programming crash course, we have implemented all the functionality that we aimed for. The only problem is that we have ended up with quite a long program that is somehow both difficult to handle, when placing instruction blocks, and also difficult to read, when we look at the instructions, trying to understand what the program does.

In this chapter we are going to see how we can simplify things by turning groups of instruction blocks into external functions that the main program can call by name.

The first thing to do is to have a look around the program and try to distinguish groups of blocks that implement a specific functionality. Let's take, for example, the two blocks that initialize the two variables "line\_sensor\_status" and "distance\_to\_obstacle":

![](/assets/Img.5.30.1.jpg)

\[Image 5.30.1: A likely candidate to become a function\]

These two instruction blocks can be seen as an entity and therefore can be turned into a new single block, also known as _function_. To create this new block we go to "Data&Blocks" \(1\) and there we click on "Make a Block" \(2\), like shown in the picture below:

![](/assets/Img.5.30.2.jpg)

\[Image 5.30.2: Where to create a new block \(a function\)\]

There will open a window where we can give our new block a name. Let's call this one "read\_sensor\_data". We type the name into the give text box and when done click "OK":

![](/assets/Img.5.30.3.jpg)

\[Image 5.30.3: The "New Block" window\]

Notice how there is an "Options" button that we don't need to use here. We we will see more of it later on.

There will appear a blue "define" block and we should connect the two "set" variable blocks to it like this:

![](/assets/Img.5.30.4.jpg)

\[Image 5.30.4: The new "read\_sensor\_data" function\]

We notice there's a new block available, now, in "Data&Blocks", named "read\_sensor\_data". We can drag and drop it, like any other instruction block, and place it to be part of the program. Whenever reached by the program, this block will execute those two inctructions we put aside, or better: it will execute function "read\_sensor\_data" \(Image 5.30.4\).

We need to place a call to the function at the begin of the forever block, at the exact spot where the two "set" variable blocks used to stand, replacing them:![](/assets/Img.5.30.5.jpg)\[Image 5.30.5: Calling the new "read\_sensor\_data" function\]

Let's see if we can distinguish another group of instructions that seem to implement a specific functionality, together. Let's take, for example, the following group of instructions:

![](/assets/Img.5.30.6.jpg)

\[Image 5.30.6: Another candidate to become a function\]

This is a big chunk of blocks that can be described as doing one single thing: have the mBot follow a line.

Following the same procedure, like before, we can create a new block: Data&Blocks &gt; Make a Block and give the new function a suitable name, say "line\_follower".

This time the function needs input, though: it needs to know the status of the line sensor. Therefore, in the "New Block" window, we do click on "Options", this time, and then we choose "Add number input". This will create a new attribute spot in the new block. Let's give this attribte a name by typing "line\_value" and when we have everything like shown in the image below, click "OK".

![](/assets/Img.5.30.7.jpg)

\[Image 5.30.7: Creating a new block that can take a number as input\]

Now, we should move aside that big group of blocks shown in image 5.30.6, breaking them off the main program and connect them to the "define" block, which is the start block of the function. In addition, we need to replace the "line\_sensor\_status", in the function, by the new "line\_value" input attribute. Just drug and drop it like shown in the image below:

![](/assets/Img.5.30.8.jpg)

\[Image 5.30.8: The new "line\_follower" function\]

Last step, we must call this new function, from within the program. In other words, we must place the new block in the "else", where the displaced group of blocks used to be, like shown in the image below:![](/assets/Img.5.30.9.jpg)\[Image 5.30.9: Calling the new "line\_follower" function\]

The function call is not ready yet, though. We need to make sure that the program will pass the status of the line sensor, which is stored in variable "line\_sensor\_status", as an attribute to the function. To achieve that, we need to take the "line\_sensor\_status" variable block and drag and drop it in the "line\_follower" block \(1\) as an attribute: ![](/assets/Img.5.30.10.jpg)\[Image 5.30.10: passing an attribute to the function\]

Now, when we run the program and the execution reaches the "line\_follower" block, the program will call function "line\_follower", passing it the value of variable "line\_sensor\_status" \(2\). What will happen is that the value of "line\_sensor\_status" will be copied to local variable "line\_value", so that the function can use it.

Once again: "line\_sensor\_status" belongs to the main program when "line\_value" is used locally by function "line\_follower".

We can then check the program for more things that can be turned into functions, simplifying the main body.

Instead, let's "Upload to Arduino", for the time being, and check if the program executes like before, making sure we didn't mess it while creating functions.

Keep in mind: functions help organizing programs better by breaking them down into smaller parts, instead of keep building on one monolithic program that is both difficult to edit and to read and understand what it does.

The mBot has preserved all the functionality we aimed for: it can follow a line, it can detect an obstacle and make a U-turn. Only now our program is better organized, too. The instructions are more readable.

We should now save the program and all the good work we have done with it and proceed to the next chapter and discuss things that our students can actually do, going forward.

### Exercises

Exercise 5.30.1: Locate in the program a different group of blocks that has meaning to turn them into a fuction. Create a new block with them and replace the instructions in the program by a call to the new function. Think well whether you need to pass values as attributes.

### Questions

Question 5.30.1: What is the criterion for choosing a group of instructions to create a new function?

A. The instructions are all of the same colour.

B. They are nested in a control block \(either an "if" block or a loop\)

C. They need to set values to variables.

D. They seem to implement together a specific functionality.

_Answer: D_

Question 5.30.2: How does the program pass a value to the function?

A. By passing the value as an attribute during the call of the function.

B. By passing the value as an attribute at the begin of the main program.

C. By initializing a variable to zero.

D. The main program never passes values to functions.

_Answer: A_

