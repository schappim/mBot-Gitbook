# Section 5

---

## Chapter 29: Using a button to start and stop

---

In this chapter you will learn about:

* How to 
* How to 

---

On the mBot, on the right side, there is a little board button that can be programmed to cause a reaction by the mBot. We can program it, for example, so that when the robot is powered on, the wheels either start or stop, by pressing it. Again, there are multiple ways to implement this behaviour and in this chapter we are going to see one.

![](/assets/Img.5.29.1.jpg)

\[Image 5.29.1: The board button\]

Let's continue with our program of the previous chapters and create a variable named "button\_toggle" that will be used to hold the status of the board button. We will be assigning just two values to this variable:

**-1** for having the wheels on

**1** for having the wheels stopped

First, and since our program will have the wheels spinning when loaded, let's initialize this variable to -1, at the very start of the program like this:

![](/assets/Img.5.29.2.jpg)

\[Image 5.29.2: Initializing the "button\_toggle" variable\]

For the rest, when the board button is pressed, we need to invert its value, assigning the opposite status to it. One simple way to do that is by multiplying its value by -1. If it was -1, it will now become 1, and vice versa. Here's how to do that:

![](/assets/Img.5.29.3.jpg)

\[Image 5.29.3: Inverting the status of the board button\]

Here, if the board button is pressed, then we set the opposite value to the "button\_toggle" by multiplying its current value by -1. The "on board button \[pressed\]" can be found in the \(navy blue\) "Robots" segment.

One last thing we need to do is, is check the status of the board button \(kept in variable "button\_toggle"\) using an if block, like this:

![](/assets/Img.5.29.4.jpg)

\[Image 5.29.4: Checking the status of the board button\]

If it is 1, we should procceed with the all the lot of instructions we created previously for trying to keep the mBot on track. If it is -1, we should just stop the wheels. That means that we should move all these instructions within the if \(board button status = 1\), and add a stop instruction \("move forward at speed 0"\) within the else \(board button status = -1\) 

Here's how to combine these new instructions in the program:

![](/assets/Img.5.29.5.jpg)

\[Image 5.29.5: The new modifications\]

~~**~~~~~ {UP TO HERE BY DIMITRIS}**~~

This will be the trigger for the wheels to start spinning and for the operation of the robot as a line follow to actually begin. Once I had enough of it, I would like to be able to press the same button again and get the robot to stop operating. To do that, cut back to the robot's section and look for the button block. There it is, so there's an on-board button.

Just going to put it here temporarily and just to give me some more space in my canvas. Here it is. This block simply returns the state of the button whether it's pressed or not, but I also need a variable. I'm going to use the variable to help my program to remember what it's supposed to do depending on the state of the button.

For example, if I press the button for the first time when I turn the robot on, then I need a variable so that I can record my instruction to the robot to start operating. I need a variable because the robot will keep then checking that variable to see if it's supposed to continue operating or not. In a while later, when I stop the robot by pressing on the button again, I want to change the state of the variable.

So that then the robot every time that it checks, the state of the variable will know that it's supposed to stay stopped. I hope it make sense, but I'm going to implement it and show you how it's supposed to work in reality. Let's make a new variable and call it, Button Toggle. Like that. To start, I would like to give my button toggle variable an initial state.

I'm going to use minus one, because this value allows me to do a simple calculation later on with the button. And I'm going to then only need to check of whether the button toggle state is minus one or plus one. Again here, there's many different ways you can go about implementing this functionality, but I think that this is simple enough as you'll see in a minute.

I'm going to put that right in the beginning of my program. This way when the mBot starts, it will look at the value of a button toggle variable. If it's minus one, then the robot will start-stopped. That sounds like a control statement doesn't it? What we're going to do is to use an if statement that will control the state of the button. Let's put this together.

If button toggle is +1, then we want everything that we've got inside our program that controls the movement of the robot to go ahead as already set. Otherwise, we'd like the robot to stop. Just going to our operators and use the equality operator and then in data blocks and use the button toggle variable and compare that against one.

Inside the first block of the if statement, I can drag this whole part of the code and just insert it there and move that back here. Just scroll towards the bottom. Now, what I would like to have in the button is for the robot to simply stop, so I'm just going to drop one of these in, and run forward at speed zero and this is going to cause the robot to stop.

One thing that I'm not yet doing is to update the button toggle variable. I'm only testing its value here, but I haven't actually done anything with the button yet. The button, on-board button block is just hanging here by itself. For that, I need to use another If Statement and it will work like this. If the on-board button is pressed, then what I'd like to do is to reset the button toggle variable to its exact opposite.

Use an operator, I'll do the multiplication operator and just take whatever value button toggle has in it -- I'll try that again, it worked the first time. Just take whatever value that button toggle variable has in it and multiply it by -1. Just place that in here. The idea here is that if currently the contents of button toggle variable is -1, then multiplying it by -1 will produce a one, and that would release the breaks and the mBot will start following the line.

If the mbot is following the line, it means that button toggle currently is +1, and multiplying it by -1 will turn it negative and the mBot then will stop. I need to put that also at the beginning of the forever loop. Okay. Now this should be it. I will try to upload the program to the Arduino now and see if pressing the button allows me to start and to stop it. Let's connect it. Turn it on.

Checks your reports, cap six, and upload to Arduino. Okay. Lets try the button. Pressing the button should start the wheels. Yes. Pressing again should stop the wheels. Okay. Let's try again. On, off. On, off. Okay. It seems like it is working. Let's go and try it out on the track now. Back on the track, I've got the mBot is already turned on.

Wheels not spinning, so I'm going to press the start button to let it loose. Off it goes \[audio silence\]. Okay, so we are good with the button and that's actually the last bit of functionality that I wanted to introduce to the mBot, at least in the context of this crash course. Before I go, there's just one more thing that we need to do. You obviously noticed that this program so far has grown to quite a large size.

What I'd like to do is to show you a way to break down this long piece of code into smaller components that are easier to manage, which in programming terms is called, a Function. I want to take some of these instructions and separate them from the main body of the program into smaller easier to manipulate and to manage functions. And then call those functions as needed in order to execute the exact same functionality. So we'll do that next.

