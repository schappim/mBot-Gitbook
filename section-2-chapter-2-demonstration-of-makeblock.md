# Section 2

---

## Chapter 2: Demonstration of the MakeBlock

---

In this chapter you will learn about:

* ---

In this lecture, I would like to show you the three applications that you can run on a tablet computer. In this case, using your IPad to control your mBot. These three applications are mBlock, mBlockly and Makeblock. Each one of those applications emphasizes a certain aspect of programming and controlling the mBot. We are going to demonstrate what each one does so you can get an idea of how you can use them.

### MakeBlock

It is a good idea to start with the Makeblock app as it is one that allows you to actually control your mBot without doing any programming at all. Instead, when you start the application, you see a lot of pre-existing apps that you can execute right away, instead of programming the mBot yourself.

After starting the app you see all kinds of mBot types, the simplest one called _mBot_. The ones marked with M+ need some add-on pack \(like, for example, the six-legged robot extension\), in addition to the mBot.

We are going to start with the basic mBot app. After clicking on it we get to see a set of controls:

1. control of the movement
2. numerical reading of the distance between the sensor and an object in front of it
3. numerical reading of the light sensor
4. on/off switch that will get the robot to execute a random movement
5. buzz button that will activate the buzzer and make some noise
6. sprint button that will get the robot to take off at maximum speed

Tapping on the "Design" tab reveals additional components that can be draged and droped onto the canvas.

Before anything, of course, we need to connect the mBot to the iPad and here's how to do this:

#### Connecting the mBot to the iPad

First thing to do is to turn the mBot on by toggling the power switch. After that we should be able to see a blue LED blinking, on the mBot. This is the Bluetooth module waiting to be connected to a Bluetooth device. That can be your smartphone, your tablet or your desktop computer, if it has got a Bluetooth module integrated.

In your device, tap onto the Bluetooth icon that is blinking on the top right corner of the screen. That will get the app to start searching for an mBot, in the vicinity, ready to connect. In case you see the message "Device found, please get closer", just get the mBot a little closer to the device. And that is actually all it takes to complete the connection between the app and the mBot.

#### Trying out the different controls

Now we should be able to make a first attempt to change the color of the LEDs on the mBot. Touch the color wheel and try some color. Touching the red, or the blue, for example, should turn the mBot LEDs accordingly. And that is what this simple color wheel does.

Next, we can try the ultrasonic sensor gauge. Put your hand, or some other object, like a book, in front of the sensor and slowly move it closer to the sensor and you should be able to see the ultrasonic reading, in the app, changing.

Next, let's try the brightness. Try and cover the top of the mBot, where the sensor is located, and you can should be able to see that the corresponding reading in the app increases. Remember to turn off the LEDs on the mBot first, for better results. If you don't, the light they produce will feed into the sensor, probably causing the brightness line in the cart to fluctuate. You can always turn the LEDs on and off by going to Design Mode \(just click on "Design" on the top of your screen\).

Obscuring the light sensor will drop the reading down. The numbers you see on the left are not particular light measuring units but rather an analog input number of the mBot: when the mBot is connected to an analog device, like the light sensor, it produces a number that represents the state of that sensor meaning, when the sensor picks up little light, their number reduces, and when the sensor picks up more light, then the number increases.

Following up we can test the buzz button. Press it and you should hear a noise.

Next we can try and control the mBot. The control lever is very much like a joystick. Try all different directions with it and you should see the mBot react accordingly.

Before testing the sprint button make enough space for the mBot to run. You can always lift it up in the air, before it smashes on anything. Keep in mind that the sprint can be reset by using the joystick.

Clicking on random will produce some random effect on the mBot like turning the LEDs on etc.

#### The code behind the controls

It is interesting to see how are all these actions attached to the controls. To have a look at the mechanics behind the controls we should go back to "Design" tab. Let's have a look, for example, at the "Sprint" button. Tap on it and in the menu that opens choose "Code" and the actual code that is triggered when you press on the sprint button will appear.

\[CODE IMG HERE\]

The code is actually self explainatory as it is very close to the natural language: When the button is pressed run forward at speed 255 \(which is the maximum\), wait for five seconds \(before proceeding to the next command\) and then stop moving.

Notice there's an event block there about what should happen when the button is released. It is empty, ready for you to put your ideas and orders, there. 

Let's say, for example, that we'd like to hear a note when the button is released. Click on "Display" on the toolbar, on the left, and different command blocks should appear. Drag and drop "play a note" just bellow "when button released" taking care that they fit one into the other, like jigsaw pieces.

 I can choose a particular note, let's say, \[background noise\]. This one sounds good. F5. I'd like to play this note for one second. Now, I've just done a little bit of reprogramming about the action that the sprint button should take when it's pressed and in this particular case, when it is released.

Let's go back and go back into play mode again and see what happens. I am going to lift the mBot so that it doesn't smash into my instruments and just have this its wheels freely rotating and I'll press on this sprint button. There you go, and with the joystick to reset. I will do this again. This time I am going to press on the sprint button and hold it and then wait for a few seconds before I release it and now let's see what the difference is.

So pressing and holding, and I am about to release it now and you can hear the noise. You can hear that when I removed my finger from the sprint button, the mBot produced that small noise through its buzzer as I specified. I would like to make one more improvement. I would like to be able to \[machine buzzing noise\] release the button like this \[beep sound\] and not only make the buzzing noise, but also stop the wheels from spinning. So how can I do that?

Let's go back to design mode and let us tap on sprint and code and then I want to do something else here in this when button released event. What I want to do is to go to the move menu and use the stop moving component and just put it here, like that. So now what happens is that when the button is released ,the mBot is going to play the F5 note for one second and then stop from moving.

Let's try this out, so back to play mode. I am going to hold the mBot up and press on the sprint button and hold it \[machine buzzing noise\] and now I am going to release it \[beep sound\]. There is a noise and a second later, the wheels stop spinning. Great that is exactly what I wanted and there is lots more that you can do for example if you are curious about how the buzz button works, just tap on it while you are in the design mode and check out the code. You can see that that's what the code does.

It has two conditions, two events that this button will respond to. The first one is when button pressed, the second one is when button released. So when button pressed, I want to play a note and now that you know how to program additional actions graphically, you can say, let's say I would like to go to display menu and play another note, perhaps try this one here, another note when the button is released and then change that to \[beep sound\] C6, all right.

Let us go back the play mode and press on the buzz button \[beep sound\], there we go \[beeping sound\]. Suppressing C5 and then releasing F5. Now, there's lots more. Go back into the design mode just to show you a couple of other things. So in terms of moving your mBot, you can also use this kind of controller with the four directional buttons instead of the joystick. You've got a button of course, sprint, which is pre-programmed but that you can reprogram and you have a few toggle switches as well.

With the display programming options, you've got again buttons like buzz and random. You've got the RGB LED color wheels, so you can choose any color for your RGB LEDs. You've got a radar warning button toggle switch, lightness button. Actually just try that out, it is quite interesting. When you turn it on, you can see that the intensity of your LEDs increases and then move it all the way to the left and then the LEDs go off. Let's go back to design mode. You can also play music \[laughs\]. It's got a little piano here. I am not going to drop it because there's not enough space on my canvas to drop the little piano or note selector. So I will have to make a bit of room.

Let's tap on the lightness box and delete it, it is fine and the same thing with sprint, delete the sprint button. Now to make some room for my music box. Back to play \[beep sound\]. It's not very responsive. That's one of the issues that I want to discuss in a minute. \[beep sound\] It has quite a bit of a lag between the time that I press on the button and the time that the sound actually comes out of the buzzer.

That is going to sense. In the sense menu, I've got a bunch of items that connect to the sensors that are on board. We've got the ultrasonic in two versions, the numerical and then the gauge with the line graph version and same thing with the brightness, we've got the numerical version and then the line graph version as well.

For custom, you have all of these components but that these are now programmable. Another interesting addition in one of the newer versions of this application is the draw and run options. Let's go into that and have a look. This gives you a canvas in which you can do a little drawing and basically design the path that you would like your mBot to go on. Actually I will make it a bit zig-zag like that. When you press play now, your mBot will try at least to follow the path that you have drawn, let us try it out.

Not enough space on my desk. But you can put this on the floor. You can see that the mBot will approximate the path that you have drawn on the path control canvas \[laughs\] and the mBot turned on my power supply. Not as accurate as this may seem, you can do the experimentation yourself but the path that the mBot actually follows is an approximation of the path that you have drawn on the path control widget.

Okay, so you can go on and create your own user interfaces using make block like I've done here for a few more examples here. For example, the DC motor allows me to independently control each one of the two motors. This one is DC motor number two \[machine buzzing noise\] and this one is DC motor number one. Those two widgets can have independent control. We've got the brightness sensor connected and of course my joystick. It is just a user interface that I put together really quickly myself.

Most of the components that you can drag and drop on the canvas are pre-programmed. You don't need to do any more programming, you can just combine them into whichever way that you like to build some useful means of controlling your mBots without doing any programming at all. Now, what if you actually do want to do a bit of programming? Well, for that, you can use mBlock.

