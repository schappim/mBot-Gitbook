# Section 5

---

## Chapter 30: Custon blocks \(functions\)

---

In this chapter you will learn about:

* How to 

---

At this point, in this mBot programming crash course, we have implemented all the functionality that we aimed for. The only problem is that we have ended up with quite a long program that is somehow both difficult to handle, when trying to order the instruction blocks, and also difficult to read, when we look at the instructions, trying to understand what the program does.

In this chapter we are going to see how we can simplify things by turning groups of instruction blocks into external functions that the main program can call by name.

~~**{UP TO HERE BY DIMITRIS}**~~

This is a common technique in the world of programming where we compartmentalize functionality and then this functionality can be easily referred to from within our program. I'm going to demonstrate what I mean by this, just to try and keep things simple.

The first thing to do is to have a look around a code and see if we can distinguish groups of blocks that implement a specific functionality. For example, how about this bit here? The code right here is the part of the program that implements the actual line following algorithm. Another bit of code like this bit here is the bit that implements the functionality of the robot in dealing with running out of line or they’re actually finding an obstacle in front of it and then dealing with that obstacle.

We got a bit more code at the top that simply gets the readings from the two sensors and updates two variables. Things like that, we can move outside the main body of the program and turn into functions. Let's do that now. The first thing to do is to create a new block which is the equivalent of a function. Inside the data end blocks sections of the scripts, there is -- I'll do that again. There is a Make a Block button. You click on that and you can create your first block. I would like this block to deal with reading the sensor data and updating the two variables. Let's call it Read Sensor Data, a sensible name.

There's a few options here so that your block can do things such as receive value from whichever part of the program is calling it and then assign it as what's called a local variable. Things like that, but we're not going to worry about this for now. We're just going to create a simple block. Here's the header for that new block. The next thing to do is to drag some of the code or to drag the code that we want, the read sensor data block to contain. It's this code here. I'm just going to drag that in here and of course, because of the way that the scratch program works and the editor works alongside the two set blocks that I wanted to drag only, I also dragged along everything else it followed.

We need to move that part of the code back inside the forever loop. I've got a new custom block called Read Sensor Data. To restore the original functionality of my robot, I need to call this block from the very top of the forever loop. We'll do that and we'll drag the Read Sensor Data block and place it at the beginning of the forever loop. At this point, I've got the exact same functionality. My program is going to start, it's going to enter the forever loop. We will see that here, I'm making a reference to a block called Read Sensor Data which is defined right here. It's going to go inside the block, execute these two blocks and then continue where it left off.

Let's do one more and then I will leave the rest up to you to change as you see fit. Just experiment with this. The other part of the code that I would like to turn into a custom block, is the part where we implement the line following functionality. That code is right here, this bit. I'm going to create a new block, I’m going to call that Line Follower. I would like this to have a input now. I would like this to have the input and that input is the state of the sensor. The state of the sensor will be input to the Line Follower block. Let's call that Line Value. This allows us to create blocks that have parameters and then those parameters can be used inside the block just like any other variable.

I'm going to say okay, and here is the header for the new block. Then I will populate that block with the code inside here, inside this part of the if/else statement. This is where we have a line following code. We're going to drag that over and put it here. Of course, I need to be able to call the Line Follower block. To do that, I'm going to drag the Line Follower block and put it where this bit of code used to be. Remember that we need a parameter here and the parameter that I want to pass is the Line Value, so the value that the line sensor has returned. I need to grab that line sensor status and put it in here.

Because now inside our block we have replaced the original line sensor status with a local variable line value, which eventually contains the same value but it's got a different name. One, Line Value is the internal name that is used inside the block, while line sensor status belongs to the outside program to the whole program. Just going to move that Line Value variable and replace any reference of the original line sensor status. Just like that. Okay, so this is what our new program looks like. If you look around the original program, there are still things that you can do to simplify it and convert some of its components into external blocks, custom blocks.

I think it's good enough for now. I’d like to upload that and make sure that my robot still works. Plug it into the USB. Actually, I don't need to turn it upside down because I've got the button functionality. Connect to comp six. Right click on the input header and upload to Arduino, and upload to Arduino, all done. Let's see, does it still work? I'm going to press the button, it looks like it is. All right. Let's go and try it out then on the track and hopefully everything would go well. The input now contains the last version of the program. It's supposed to behave in the exact same way as the previous version, it's just that now it's more organized using custom blocks than just having a one monolithic piece of code.

Let's start it and see how it behaves. Yes, it looks like it behaves exactly like it did before. Great, okay, that's it. At this point, we've got the mBot behaving in the way that we planned for. It can follow a line, it can turn around when it reaches the end of the line and detects the obstacle in front of it. We were also able to improve the construction of our program by using custom blocks. Let's wrap it up in the next lecture and discuss things that your students can actually do going forward.

