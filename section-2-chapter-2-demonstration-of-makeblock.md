# Section 2

---

## Chapter 2: Demonstration of the MakeBlock

---

In this chapter you will learn about:

* 
---

In this lecture, I would like to show you the three applications that you can run on a tablet computer. In this case, using your IPad to control your mBot. These three applications are mBlock, mBlockly and Makeblock. Each one of those applications emphasizes a certain aspect of programming and controlling the mBot. We are going to demonstrate what each one does so you can get an idea of how you can use them.

### MakeBlock

It is a good idea to start with the Makeblock app as it is one that allows you to actually control your mBot without doing any programming at all. Instead, when you start the application, you see a lot of pre-existing apps that you can execute right away, instead of programming the mBot yourself.

After starting the app you see all kinds of mBot types, the simplest one called _mBot_. The ones marked with M+ need some add-on pack, in addition to the mBot.

There's a few others, you can see this one here for example, again, Mplus, this one allows you to control your mBot with its six-legged robot pack extension.

Let's start with something very simple. Let's go to the mBot app and you can see that already, we've got a set of controls here. So we've got the set of controls. This one here allows you to control the movement of the mBot. This gets a numerical reading of the distance between the sensor and an object in front of it. This one takes the reading from the light sensor inside the mBlock controller. This one, when you switch, there's a toggle switch. When you switch it on and the robot will do some random movement.

They've got button that allows you to activate the buzzer to make some noise and once you press the sprint button, as you can probably guess, the robot will sprint, will take off at maximum speed. Apart from what you see here, if you tap on the design tab, then you can reveal the various components that you can drag and drop onto the canvas. For example, if you want to do a display of lights, then you can drag this little component here onto the canvas. Then go back to play note, so tap the play tab and then by sing the color wheel, you can change the color of the integrated RGB LEDs. Of course nothing's happening yet because I haven't connected my IPad to the mBot.

Let's do that now. First thing to do is to turn the mBot on. \[Just move this to the side. All right, you can see that I've got a blue LED and it's blinking on the Bluetooth module. Move that a bit here so you can see the blue LED blinking. This is the location of the Bluetooth module. When the blue LED is blinking, what this means is that the mBot is waiting to be connected to a Bluetooth device and that can be your smartphone, your tablet computer or your desktop computer if it's got a Bluetooth module integrated.

In this case, I'm going to connect my mBot to my IPad. To do that, I will tap onto the Bluetooth symbol or icon that is blinking, top right corner of the screen. You can see that now the application is searching for an mBot ready to connect in the vicinity. It says, "Device found, please get closer." I need to get my mBot a little closer to the device and that's it, connection completed.

Now, let's try with the lights first. I'm going to change the color wheel. Let's go a bit more towards the blue. Yes, the LEDs are turning blue. Let's go to the red, okay and the LEDs are turning red. That's what this simple color wheel does.

Next, let's try the ultrasonic sensor gauge. I'll use my hand as a target and as I'm moving my hand closer to the sensor, you can see that the reading of the ultrasonic gauge is changing. Like a bit distance is increasing. Good. What about the brightness? I'm going to cover the top of the mBot where the sensor is and you can see that the reading fluctuates and then the reading increases. It fluctuates a lot because, remember that I've got my LEDs that are also producing light that feeds into the sensor.

I'd like to turn the LEDs off. The simplest way to do it is to go back to design mode and by doing so, the mBot gets reset so the light goes off on the edge of the LEDs. Back to Play. Now that I've turn the integrated RGB LEDs off, I put my hand over the mBot again to get in light going to the light sensor and see what the reading in the gauge is. All right, you can see that the reading drops down to about 390. This is not a particular unit by which we measure light, it's just the analog input number on the Arduino.

When the Arduino is connected to an analog device like the light sensor, what it produces is just a number that represents the state of that sensor. In this case, when the sensor is picking little light, their number reduces, and when the sensor picks up more light, then the number that **\[unintelligible 00:07:19\]** reports is increasing. That's why now I've got a lot of light coming from my desk lamps here hitting the light sensor. You can see that the intensity increases in the gauge.

Let's make some noise. Press the buzz button. It has a noise. Let's control it, so I'm going to reverse. I'm going to push that lever back and reverse my mBot. There you go. Turn towards the right. Good, towards to left and move forwards. There you go. This is like a joystcik. I'm going to move back a bit into the sprint very carefully not to smash into my instruments here. Let's sprint by pressing the sprint button. Okay, reset by using the joystick. And there's this something random just by switching of and switching on the random button. Random light LED show.

Okay, now all of the actions that I've shown you are actually attached to these controls. To show you how that works, I'll go back to design tab and let's have a look at sprint. If you're curious to know how sprint works, just tap on it and then tap on the code button to have a look at the actual code that is triggered when you press on the sprint button. You can see that when the button is pressed, then run forward at speed 255, which is a maximum speed. Then wait for five seconds and then stop moving. It doesn't say anything about what to do when the button is released but there's another condition that you can program.

For example, I can get it so that when the button is released to play a note, I can choose a particular note, let's say, \[background noise\]. This one sounds good. F5. I'd like to play this note for one second. Now, I've just done a little bit of reprogramming about the action that the sprint button should take when it's pressed and in this particular case, when it is released.

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

