# Section 4

---

## Chapter 22: The "if" and "if...else" control structures

---

In this chapter you will learn about:

* ---

In the last chapter we got ourselves an mBot that blinks its LEDs blue and red, depending on the distance between its ultrasonic sensor and a target object. That has given us understanding of how the ultrasonic sensor and the forever loop work.

In this chapter we will see how we can get the mBoard to make decisions, depending on sensor readings, like the ultrasonic sensor. Towards that goal, we're going to build a new program that, once more, uses the LEDs and the distance sensor only this time it turns the LEDs into a particular colour depending on the distance between a sensor and the target: green when it is far away, orange when it gets closer, red when it is too close.

In order to make desicions we use the "if" and "if...else" blocks that we can see in the image below:

![](/assets/Img.4.22.1.jpg)

\[Image 4.22.1: The "if" and "if...else" blocks\]

These two control blocks can evaluate a given condition and execute some nested instructions, depending on whether this condition is true or not. Blocks suitable to be used as conditions can be found in the \(green\) "Operators" family of blocks:

![](/assets/Img.4.22.2.jpg)

\[Image 4.22.2: Operators like these can compare values and be used as conditions\]

You will notice that such blocks have angular sides that make them fit in the condition spot, after the "if" word:

![](/assets/Img.4.22.3.jpg)

\[Image 4.22.3: Where to place the operator block\]

Let's create a new program: File &gt; New

Now, let's create a variable distance and by adding blocks and fit them together let's compose the program shown in the image below:

![](/assets/Img.4.22.4.jpg)

\[Image 4.22.4: The program\]

We notice that the if...else block is nested within the forever loop. Port3 referes to the port where the ultrasonic is connected on the mBot. We should always check to in order to get such attributes right.

Here's how to read this program: Get a reading from the ultrasonic sensor and store it in the "distance" variable. Then check this value, stored in "distance" and if it is greater than 30, then set all LEDs to green, else set them to blue. And all than, over and over again, since it's nested in a forever loop.



~~~~~~~~~

Let's start the process with a brand new program. Here's a brand new program, we're close in so we get a bit more space to work with. As always, we will start with the mBoard program header block and because we want the program that we are about to run to continuously run without interruption forever or at least until we turn it off, we are going to use the forever loop. Now, let's think about what the objective is, we want to control the color of both LED's depending on the distance between the object and the sensor.

The first thing that we need to do is to take a reading out of the sensor and to do that we need a variable. Let's go ahead and create a variable just like we did before the previous example, we call it distance. And take the distance or the set distance log and just place it at the beginning of the forever loop so that every time we go through a new cycle inside the forever loop, the first thing that we do is to get a distance measurement from the sensor and store it inside the distance variable.

We got this set distance block and then we need to go into the robots section and find the ultrasonic sensor block and use it to replace that fixed value for the distance variable. Now, ultrasonic sensor is connected to the PORT 3 so that's good. Then, lets consider what is it that we would like to do. What we would like to do next is to make a decision, we'd like the LED's to light up in the particular color depending on the distance between the sensor and the object in front of it.

If the distance is, let's say, greater than 30cm then I would like my LED's to be green, so I use the keyword IF that indicates that a decision now has to be made. Now, the keyword IF also happens to be a keyword in a programming language and if we are going to the control section we'll see that there is an IF statement here, looks like this. There's also another one that looks like this. That both start with the IF statement however the second version of the IF statement, the IF block gives us the option to take an alternate course of action if whatever the test that we are using up here in the beginning turns out to not be true.

Let's go back to the question that I asked, if the distance between the sensor and the obstacle in front of it is greater than 30cm, then do something in the first area right under the IF statement but if it isn't, so if the distance is less than 30cm then I would like to do something else. That's what the ELSE keyword does. It gives us the ability to define an alternative course of action for the robot. That is why I'm going to throw away the first version of the IF statement and just keep the second version only.

Before I drag it into the forever loop, I'd like to continue the construction of the IF statement here, on its own. Let's talk about the condition that we are testing for. We are testing for distance, if distance is larger than 30cm, that sounds like we need an operator here that larger than the keyword is an operator. We go into the operator's group and have a look inside here. Notice that we've got of bunch of operators, we've got of course, the arithmetic operators, minus, times, division. We also have comparison operators, less than, equal and larger than.

In our case we want to test for larger that it drags it larger than operator, just put it here inside, in between the IF-AND event and to notice how that fits. Looks like we've got an angled side instead of a curved side for this block, which means that it will fit in here. We now can compare two values together, one against the other. Now the first one is the distance variable, the contents of the distance variable which contain a number that was reported by the ultrasonic sensor. To grab that I've got the data mBlocks and grab the distance variable and place it in the first box of the operator.

And then I just need the fixed value 30 because that's where I'm testing for. I'm testing for distance being larger than 30. What is it that I'd like to do if distance is larger than 30? Well, if distance is larger than 30 and I'd like to change the color of the onboard RGB LED's, so I'm going back to the robot section and I will grab the set LED on board block, and I don't want to distinguish between left and right RGB so I'm just going to use OR. And I would like to turn that into green.

Everything is okay, there's no imminent danger for our robot so we're going to turn the green light on. We are okay with the condition of distance being greater than 30. Now, what if it's not greater than 30? What if it's less than 30? Well, let's say that for now we'd like to just have the LED in a different color, to show a different color. Let's make it blue, for example, to do that again similarly we're going to get the set LED block for both LED's and I will make that-- like that.

With this IF-ELSE statement we've covered the two conditions of what happens when the distance is greater than 30 and what happens when the distance is not greater 30, therefore less than 30. I'm going to drag this block inside the forever loop and just insert it there. Before going any further, I would like to test that my sketch actually works, the program actually works. Let's connect to COM-6 and right-click the header and upload this program to the Arduino or to the mBlock.

Okay, so here's my obstacle, my hand is my obstacle. Here's my hand playing the role of the obstacle and it's over 30cm and it's about to change, and now it's less than 30 cm, you can see that now the color is blue--green--blue--There's a bit of playing around about this distance so I suppose that's just that the boundary between larger than 30cm and smaller than 30cm. But this is how it works, just worked.

I'd like to add another little feature, another decision point and I'd like the color to turn to red when the distance is say below 20cm to below that. Let's think about how we can make that happen. I'd like to do is for the LED's to be green when the distance is over 30cm, to be blue when the distance is between 30cm and 20cm, and to become red when the the distance is less than 20cm.

Again, there's a few different ways you can go about implementing this code in your program, but I'm going to show you one of them. Of course, it involves using another IF statement here, another IF-ELSE statement actually. Let's look at the new condition, if the distance is greater than 30cm that's covered, the second condition that I would like to insert here in the IF block is, the condition of distance being larger than 20cm now. It's the same conditional block, it's this one here. And I'll go into data mBlocks and pick the distance block that represents the distance variable and putting a fixed number 20, for 20cm.

What I'd like to do is that if the distance is larger than 20cm then I would like the LED's on board to become blue. If it's not true then the only alternative is for the distance to be less than 20cm, but I don't actually have to specify that because there's no other possibility. All I've got to do then is to just get the same set LED block for both LED's and turn that into red while green and blue are zero. I'm going to drag this IF block into the forever loop.

Now, let's preview this, just read this out loud before we upload it to the Arduino and see how it behaves. First, we measure the distance using the ultrasonic distance sensor and store that value inside the distance variable. Then, we check to see if that distance is larger than 30 and if it is, then we set a color of the two LED's to green. Then, we're going to go out of this IF statement because-- now, we're going to go out of this IF statement and go back up in the loop, the forever loop, that is. Pick another measurement from the sensor, store the new value in the distance variable.

Now, let's say that this variable is now 25cm, being 25cm, the first IF check would fail, because distance is not larger than 30. So, we'll go into the ELSE block. The first thing that happens in the the ELSE block is to check if the distance is larger than 20 and that turns out to be true because hypothetically now our distance contains a number 25. If it is, we're going to go into this block here which will turn the color of the two LED's to bright blue. Once that is executed we'll get out of the second IF statement, out of the first IF statement and then back up at the beginning of the forever loop.

Now, if the distance in the third and then go through the loop is say 10, which means it's not larger than 30 and is not larger than 20 then the only thing that remains to be done is to execute the block in the end of the code and that would turn the LED's to bright red. I hope that makes sense. In cases like that where you get confused about the way that a program works then you can just run through it, you can use pen and paper or you can run through it line by line manually so that you can understand how it works.

Let's upload the program to the Arduino and test it in practice. Okay, after it's finished lets try it out now. A hand is the target. We're now beyond 30cm, I'll give you a better view. We are beyond the 30cm, we need it closer so now we are just above 20cm, closer so now we are below 20cm and the LED's are red. Isn't that great?

Now, I've got a little exercise for you before we move on to the next thing that I'd like to show you. \[music\] I'd like to mimic traffic lights. Traffic lights we've got green, we've got red but we don't have blue we've got amber. How about you figure out how to change the codes of that instead of blue you could use amber.

