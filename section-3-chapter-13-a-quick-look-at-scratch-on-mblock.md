# Section 3

---

## Chapter 14: A quick look at Scratch

---

In this chapter you will learn about:

* The basic blocks for creating a Scratch program
* How to control the movement of a sprite
* How to print messages from a Scratch program
* How to execute a program
* How to add and remove blocks to and from a program
* How to repeat a segment of your program many times

---

Now that you have installed mBlock on your computer, go ahead and start it, if not already done so.

In this chapter you will not use the mBot yet. Instead, you will learn how to manipulate the movement of the Panda sprite by writing a simple Scratch program. As you do that, you will learn how to use some of the most common Scratch programming blocks.

![](/assets/2017-03-24_16-46-55.png)

\[Image 3.14.1: In this chapter you will learn how to control the Panda using Scratch\]

Let's start with the "Say" block.

![](/assets/2017-03-24_16-50-35.png)

\[Image 3.14.2: The "Say" block\]

The "Say" block allows you to print a text message in a bubble over the Panda. Select the Scripts tab from the blocks palette, and find the "Say" block at the top of the Looks group of blocks. Click on it, and while you hold the mouse button, drag the block into the Script area.

By default, this block simply prints "Hello" over the Panda, but you can change this text to anything you like. Simply click on the white text box and replace the current text with something else. Write "Hello world," for example, by clicking in the text box marked "1" in Image 3.14.3. You can also control how long you'd like the message to appear for, before it disappears. Let's make it two seconds by clicking in the text box marked "2" in Image 3.14.3.

![](/assets/2017-03-24_16-58-03.png)

\[Image 3.14.3: The "Say" block has two attributes that you can change, the Text and the Duration attributes\]

**PETER DONE UP TO HERE**

Now the weight by which I can trigger a program is by using an event. Have a look at this tab here. I've got three tabs, I’ve got scripts, costumes and sounds. The one that I'm interested in right now is the script tab. It's got various sections in here, so motion, looks, sound and et cetera. On the other side, there's the events script section. Inside the event script check section, you can see that I’ve got blocks that allow me the trigger a program. The one that we most commonly used to trigger a program to start is the green flag block.

When the green flag is clicked then they will provide the trigger that we need to start my programs. Let's use it. I'm going to drag the flag and attach it to the say, "Hello world," for two seconds block. You can see how there's a little indentation here that matches between the two blocks. That's how I know that the two blocks are compatible with each other and they can work. Now, when I click the green flag on the user interface of the mBlock application, whatever is below it and connected to it will actually execute. Here's a green flag. I'm going to click on it and Panda says, "Hello world," for exactly two seconds.

I can use other triggers of course. Let's say this one when space key is pressed. I can attach when space key or can choose any other key from the drop down menu, that’s little space. When space key is pressed then, "Hello world," for two seconds. I'm pressing the space key and we can see that panda says, "Hello world," for two seconds. You probably noticed that when I put my mouse over a block like this one, they say, "Block," and I just click on it then Panda again says, "Hello world". That is just a quick way for you to determine what a particular block does before you actually use it. It's like a preview of what the block does.

Now let's do something else. I'm going to actually remove the say block from the when block and I will delete the when block. There's two ways to delete something or to remove something from your program. The first one is to do a right click and choose delete, and they will make this blog disappear. The other way is to just drag it onto the side where it came from where you've got all your blocks for a particular section assembled. I'm going to leave that here unconnected for now and I would like to use some motion.

Going to go into the motion section, and take the move block and connect it to the trigger, the event with a green flag. We’re going to change that maybe to 50 steps because each step is very small and I'd like you to be able to see it without struggling. I'm going to get the Panda to move by 50 steps and then to say, "Hello world." Let's try that out. I'm going to move the Panda just by dragging it onto the side because it's going to move this way, towards the right of its area. Green flag, there we go, we moved by 50 steps and then it said, "Hello," for two seconds at the end.

I can do something more elaborate like let's say for example, that I would like it to move by 50 steps and then to turn by 45 degrees, and then to move by another 50 steps. Change that to 50 and then for you to say, "Hello." I can move Panda back to the beginning and press on the green flag. It happens very quickly but it moved by 50 steps as per the first block, then it turned by 45 degrees and then it moved by another 50 steps.

If this is happening too fast then you can go for a bit of control and see how there's a one second control here. I'd like to take that and put it in between the move and the turn blocks, and change that perhaps to a two. Inside the little text area, you can specify the amount of time that you’d like Panda to wait for. It could be a whole number. It could be five seconds or it could be a decimal, so it could be 0.5 seconds. You can insert the exact amount of delay that you'd like. I'm going to do that as well down here. Let's say you wait for another two seconds before you move for another 50 steps, I like that.

Let's take panda back up here. You can see now that it's pointing -- it's looking downwards at 45 degrees. Let's go back to this to the motion section and introduce a left turn sketching. I'm going to make it 90 degrees to begin with because what's going to happen is when I execute this program, Panda is going to move 50 steps forward, wait for two seconds then turn by another 45 degrees, in addition to the 45 degrees from the previous execution. Wait for two seconds, move 50 steps and I’d like it then to look horizontally again. For that reason, I'm going to turn it left by 90 degrees. Just to counteract the accumulated total 45 plus 45 degrees turn from its previous two turns.

Let's try that out, green flag, there you go. \[laughs\] Okay. Another way by which you can manipulate Panda is by clicking on this little I button and the sprites at the bottom of the window. By clicking of that, it can change the name of the sprite, you can call it mBot, for example, or mBot Panda to be more specific. You can change its direction, the way that is looking. Let's make it back to 90 degrees and things like that. They can make it disappear and so on. I'm going to put my program back to 45 degrees.

Let's do this one more time. Seconds, turning two seconds and then another 10, 50 steps and then say, "Hello," for two seconds. I’d like to show you one more thing. I'm going to remove this part of the program and delete it. I’ll actually just throw the whole thing out like that. What I'd like to do is to get the Panda to move from one end of the real estate to the other end. But I don't want to do it by just adding more steps to the move block.

What I'd like to do is to use a control structure. A very simple control structure, all of them are available under the control section, is repeat structure. The repeat structure does exactly what it says. It would repeat whatever you've got inside as many times as you wanted. What I've just done is to get the Panda to move 50 steps, 10 times. In total we're going to have 500 steps and we’ll let me do this, which is three blocks here, instead of having to worry about too much with increasing the number of steps inside the move block. It's just a lot more readable.

Every time that it moves its 50 steps, it's going to take two seconds, actually reduce that to one second since two seconds will be too much. When it finishes, I'd like it to say hello, of course, for another two seconds. I'm going to go back to the looks section and drag the block and get it to say, “Hello world,” after it finishes the 10 repeats of the 50 steps for each repeat. Let's start it. First, second, third, fourth, fifth, six, seven, eight, \[laughs\] nine, 10. \[laughs\] You probably saw me that I dragged as it was about to go past the box. I dragged it back so that it doesn't go over my scripts section.

Let’s do that again. Green button, two, three, four, five, six, seven, eight, nine, 10. Because it disappears, \[laughs\] what it goes beyond its area of movement for this pride. There's a lot more blocks which could play around with, so I invite you to experiment with those programming blocks and get your Panda to do different things like perhaps move in circle or move in a box like this, or move diagonally. You can also get it to say things depending on its location, for example. Or I can get it to change, it makes sounds, for example, experiment with the sound blocks and things of that sort.

\[music\]

Let's move on to the next topic now which involves actually having a look at how we can use the mBlock application to program the mBot robot.

