# Section 4

---

## Chapter 20: The loop

---

In this chapter you will learn:

* 1

---

Often we find ourselves in need for repetetive actions. A loop allows us to group together multiple instructions that we need to execute several times. To see such a loop in practice, let's create a new program that will make the two RGB LEDs blink in turns: the right LED will shine a particular colour, then it will go off, then the left LED will show a different colour, then it will go off and then this process will repeat again, indefinitely.

We must know, by now, how to create a new program: File &gt; New and then, since we mean to program the mBot: Robots and place the "mBot Program" onto the canvas.

Loops are found in the yellow, "Control" group of instructions. We go there, pick the "forever" block and make it the first instruction just below the header block.

![](/assets/Img.4.20.1.jpg)

\[Image 4.20.1: The forever loop control instruction block\]

Whatever is placed within the forever block opening \(1\) is going to get repeated over and over again, forever, or at least until we either turn off the mBot or replace the program that is running with another program.

We have seen how to control the LEDs. Let's pick the correct blocks and change their attributes to create the following program:

![](/assets/Img.4.20.2.jpg)

\[Image 4.20.2: The program for turning the LEDs on and off in turns\]

Reading the code: the left LED shines red for half a second, then turns off at the same time that the right LED starts shine blue for another half a second, and then turns off. And that over and over again because it is contained in a "forever" loop.

If we connect the mBot and run the program we are going to see the two LEDs blink red and blue, in turns, very much like on a police patrol car.



~~~~~~~~~

Pick up the same set LED on board block make sure that the left LED, sorry, the right LED is turned off, which means that all of the parameters should be zero. Then this is going to take me back to the left LED so back to the beginning. Once we reach the last instruction, because of the forever loop we're going to go back to the top and turn the left LED back on to red.

Wait for half a second turn the red LED off. Turn on the right LED as blue and then half a second later turn that blue off as well. Let's see first of all if it works. Check my connection so reports comm six, select comm six. \[laughs\] It’s running the previous sketch. Okay, it’s finished. Now, let's upload to Arduino. Writing and reading there you go. I've got the two LEDs alternating blue and red.

I can modify this little program slide, but just make it a little bit easier to read eventually. I can move the last instruction that turns off the right LED back up here. All right, what this now does is that I've got a nice grouping of instructions that really belong together. What the first set of instructions is saying, the first two set LED on board instructions or blocks are saying that, "Turn the left LED to red and the right LED to off."

Because all of the components are zero. Then the second block does the exact opposite. It turns on -- it turns off the left LED and then on the right LED to display a bright blue light. You can see how this syntax looks nicer to the eye and it's also easier to read and understand by another person.

This just a reminder that the same sketch even if it's very, very simple, it can be written in equivalent ways. Equivalent in terms of functionality, but in ways that make the program easier to read and then to debug and fix if you have any problems. I can make a little addition to this program and just like before, I can use a variable just say how the variable can again help to change the -- whether a program works without having to redesign the whole program.

So let's say, you can create a variable that now controls the on, actually LED on time in seconds. I’m going to use a variable to set the amount of time that I like each LED to be on and you can make it to say that in 20.3 seconds. Now, instead of the amount of time that each LED is turned on being a fixed 0.5 seconds I can make it variable.

So just like in the previous example going to move the LED on time variable into the weight blocks. Now, I can just quickly reprogram the Arduino with the new on time for each LED specified inside a variable. Let's try it out. Okay, now you can see that the LEDs are turning on and alternating faster than they did before, quick and easy way to control your lights. It's nice effect.

How about if we take this now one step further? What I'd like to do is to use the proximity sensor on the mBot to change the amount of time that each LED is turned on, depending on the distance between the sensor and an object in front of it.

For example as the object goes closer to the sensor I can get the timing to be faster. The LED will start blinking faster and there's my hand, the target or the obstacle goes further away from the sensor then pace will slow down. Let's do that next.

