# Section 5

---

## Chapter 30: Custom blocks \(functions\)

---

**In this chapter you will learn about:**

* How to create a custom block
* When to create a custom block
* How to pass values to a custom block

---

**This chapter contains hands-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will learn how to create custom functions and organise your program in a more efficient way.

---

At this point your program contains all the functionality that you aimed for. The current version of the program is fairly long though. Long programs are difficult to handle. Modifications are not easy and prone to introducing defects \(also known as "programming bugs"\). Long programs are also difficult to read, and difficult to explain to other people.

In this chapter you will learn to use custom block in order to simplify the way that your program is composed. You will not change any of the functionality, only the organisation of your program.

The first thing to do is to have a look around the program and try to distinguish groups of blocks that implement a specific and distinct functionality.

Take, for example, the two blocks that initialise the two variables "line\_sensor\_status" and "distance\_to\_obstacle", towards the top of the program \(see Image 5.30.1\).

![](/assets/Img.5.30.1.jpg)

\[Image 5.30.1: A likely candidate to become a function\]

These two instruction blocks can be grouped together as an entity and therefore can be turned into a new single block, also known as _function_. To create this new block go to the "Data&Blocks" \(1\) group and click on "Make a Block" \(2\), like you can see in Image 5.30.2.

![](/assets/Img.5.30.2.jpg)

\[Image 5.30.2: Where to create a new block \(a function\)\]

In the window that comes up name your new custom block as "read\_sensor\_data", and click "OK" \(see Image 5.30.3\).

![](/assets/Img.5.30.3.jpg)

\[Image 5.30.3: The "New Block" window\]

Notice how there is an "Options" button that we don't need to use here, so leave that alone. You will learn about the Options later in this chapter.

This process will create new block that you can drag and drop in the program pane. Notice how it is blue, with the keyword "define", and a purple "roof" over it, suggesting that this block should be used as the top block for other blocks \(see Image 5.30.4\).

![](/assets/Img.5.30.4.jpg)

\[Image 5.30.4: The new "read\_sensor\_data" function\]

There's also a new block available in the "Data&Blocks" group, named "read\_sensor\_data", which is the name you gave to your new custom block. We can drag and drop it, like any other instruction block, and place it to be part of the program.

The purpose of this block is to call the custom block from any part of your program. Have a look at Image 5.30.5. Notice that the "read\__sensor\_data"_ in Image 5.30.5 is the first block in the "forever" loop \(in the main program\). Every time the program execution reaches it, the instructions in the_ "read_\_\_sensor\_data" \_custom block in Image 5.30.4 will be executed. When the instructions in the custom block are executed, the program will continue with the next instruction in the main program.

Go ahead and drag the "_read\_sensor\_data_" block into the main program as you can see in Image 5.30.5, and replace the two "set" blocks that are there at the moment.![](/assets/Img.5.30.5.jpg)\[Image 5.30.5: Calling the new "read\_sensor\_data" function\]

Let's continue with the re-organisation of your program.

Try to find another group of instructions that seem to implement a specific functionality, together.

How about the ones in Image 5.30.6:

![](/assets/Img.5.30.6.jpg)

\[Image 5.30.6: Another candidate to become a function\]

This is a big chunk of blocks that can be described as doing one single thing: have the mBot follow a line.

Following the same procedure that you used earlier to create a new custom block, again create a new block and give it a suitable name: "line\_follower".

This time, though, the function needs input: it needs to know the status of the line sensor. Therefore, in the "New Block" window, click on "Options", and then we choose "Add number input". This will create a new parameter in the new block that can be used to pass a value to the function.

Give this parameter a name by typing "line\_value", and then click "OK" \(see Image 5.30.7\).

![](/assets/Img.5.30.7.jpg)

\[Image 5.30.7: Creating a new block that can take a number as input\]

Now, you must should move that big group of blocks shown in image 5.30.6, breaking it away from the main program, and attach it to the "define" header block, which is the start block of the function.

In addition, you must replace the "line\_sensor\_status", in the function, by the new "line\_value" input attribute. Just drug and drop the variable block into the appropriate locations in the custom block, to compose the custom block that you can see in Image 5.30.8.

![](/assets/Img.5.30.8.jpg)

\[Image 5.30.8: The new "line\_follower" function\]

Now that the custom block is defined, you need to place reference to it in the main program so that it can be called and its contents executed. In other words, you must place the new block in the "else", where the displaced group of blocks used to be, like shown in the image below:![](/assets/Img.5.30.9.jpg)\[Image 5.30.9: Calling the new "line\_follower" function\]

The last thing to do is to fix the parameter of the "_line\_follower" \_custom block. By default it is set to a constant "1", but instead you want to pass the variable_ "line\_sensor\_status\_". To do that, take the "line\_sensor\_status" variable block and drag and drop it in the "line\_follower" block \(1\) as an attribute: ![](/assets/Img.5.30.10.jpg)\[Image 5.30.10: Passing an attribute to the function\]

Now, when you execute the program and the execution reaches the "line\_follower" block, the program will call function "line\_follower", passing it the value of variable "line\_sensor\_status" \(2\). The value of "line\_sensor\_status" will be copied to the custom block local variable "line\_value", so that the function can use it internally.

_Once again: "line\_sensor\_status" belongs to the main program when "line\_value" is used locally by function "line\_follower"._

You can continue to try and more code in the main program that can be turned into custom functions, simplifying it.

But at this point, your program is already much better organised than what you had in the previous chapter. Go ahead and upload it to your mBot and try it out. The program will make your mBot behave exactly like it did before these modifications.

---

**Pro tip:**

Functions help organising programs better by breaking them down into smaller parts, instead of keep building on one monolithic program that is both difficult to edit and difficult to read and understand what it does.

---

The mBot has preserved all the functionality we aimed for: it can follow a line, it can detect an obstacle and make a U-turn. Only now our program is better organized, too. The instructions are more readable.

Remember to save the program with all the good work you have done.

---

#### **Question 5.30.1: Locate a different group of blocks that group into a custom function. Create a new block with them and replace the instructions in the program by a call to the new function. Think well whether you need to pass values as parameters.**

Answer: A good candidate is the code that involves the build-in button.The Image below show what the final program will look like after the button code is also turned into a custom block.![](/assets/2017-04-24_10-33-50.png)

---

#### Question 5.30.1: What is a main criterion for choosing a group of instructions that may be converted into a new function?

A. The instructions are all of the same colour.

B. They are nested in a control block \(either an "if" block or a loop\)

C. They need to set values to variables.

D. They seem to implement together a specific and unique functionality.

_Answer: D_

---

#### Question 5.30.2: How does the main program pass a value to the function?

A. By passing the value as an parameter

B. By passing the value as an attribute, at the begin of the main program.

C. By initialising a variable to zero.

D. The main program cannot pass values to functions.

_Answer: A_

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] You know how to create custom block without parameters

\[   \] You know how to create custom block with parameters

\[   \] You have created at least one custom block

\[   \] Your line following program now has three custom block, and operates normally

