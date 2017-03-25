# Section 2

---

## Chapter 9: Demonstration of the MakeBlock

---

In this chapter you will learn about:

* How to control the mBot using MakeBlock on a tablet

---

In this Section, we are going to see three applications that you can run on a tablet computer, like an iPad, to control your mBot. These three applications are called **mBlock**, **mBlockly **and **Makeblock**. Each one emphasizes a certain aspect of programming and controlling the mBot. We are going to demonstrate what each one does so that you can get an idea of how you can use them.

### MakeBlock

It is a good idea to start with the Makeblock app as it is one that allows you to actually control your mBot without doing any programming at all. Instead, when you start the application, you see a lot of pre-existing apps that you can execute right away, instead of programming the mBot yourself.

After starting the app you see all kinds of mBot types, the simplest one called _mBot_. The ones marked with M+ need some add-on pack \(like, for example, the six-legged robot extension\), in addition to the mBot.

![](/assets/Img.2.2.1.jpg)

\[Image 2.9.1: The begin screen\]

We are going to start with the basic mBot app, on the top left. After clicking on it we get to see a set of controls:

1. control of the movement
2. numerical reading of the distance between the sensor and an object in front of it
3. numerical reading of the light sensor
4. on/off switch that will get the robot to execute a random movement
5. buzz button that will activate the buzzer and make some noise
6. sprint button that will get the robot to take off at maximum speed

![](/assets/Img.2.2.2.jpg)

\[Image 2.9.2: The controls\]

Tapping on the "Design" tab reveals additional components that can be dragged and dropped onto the canvas.

![](/assets/Img.2.2.3.jpg)

\[Image 2.9.3: Additional controls on the Design tab\]

Before anything, of course, we need to connect the mBot to the iPad and here's how to do this:

#### Connecting the mBot to the iPad

First thing to do is to turn the mBot on by toggling the power switch. After that we should be able to see a blue LED blinking, on the mBot. This is the Bluetooth module waiting to be connected to a Bluetooth device. That can be your smartphone, your tablet or your desktop computer, if it has got a Bluetooth module integrated.

![](/assets/Img.2.2.4.jpg)

\[Image 2.9.4: The Bluetooth icon\]

In your device, tap onto the Bluetooth icon that is blinking on the top right corner of the screen. That will get the app to start searching for an mBot, in the vicinity, ready to connect. In case you see the message "Device found, please get closer", just get the mBot a little closer to the device. And that is actually all it takes to complete the connection between the app and the mBot.

#### Trying out the different controls

Now we should be able to make a first attempt to change the colour of the LEDs on the mBot. Touch the colour wheel and try some colour. Touching the red, or the blue, for example, should turn the mBot LEDs accordingly.

![](/assets/Img.2.2.5.jpg)

\[Image 2.9.5: The colour wheel\]

Next, we can try the ultrasonic sensor gauge. Put your hand, or some other object, like a book, in front of the sensor and slowly move it closer to the sensor and you should be able to see the ultrasonic reading, in the app, changing.

Next, let's try the brightness. Try and cover the top of the mBot, where the sensor is located, and you can should be able to see that the corresponding reading in the app increases. Remember to turn off the LEDs on the mBot first, for better results. If you don't, the light they produce will feed into the sensor, probably causing the brightness line in the cart to fluctuate. You can always turn the LEDs on and off by going to Design Mode \(just click on "Design" on the top of your screen\).

![](/assets/Img.2.2.6.jpg)

\[Image 2.9.6: Covering the light sensor with the hand\]

Obscuring the light sensor will drop the reading down. The numbers you see on the left are not particular light measuring units but rather an analogue input number of the mBot: when the mBot is connected to an analogue device, like the light sensor, it produces a number that represents the state of that sensor meaning, when the sensor picks up little light, their number reduces, and when the sensor picks up more light, then the number increases.

Following up we can test the buzz button. Press it and you should hear a noise.

Next we can try and control the mBot. The control lever is very much like a joystick. Try all different directions with it and you should see the mBot react accordingly.

Before testing the sprint button make enough space for the mBot to run. You can always lift it up in the air, before it smashes on anything. Keep in mind that the sprint can be reset by using the joystick.

Switching "Random" on will produce some random effect on the mBot like turning the LEDs on etc.

#### The program behind the controls

It is interesting to see how are all these actions attached to the controls. To have a look at the mechanics behind the controls we should go back to "Design" tab. Let's have a look, for example, at the "Sprint" button. Tap on it and in the menu that opens choose "Code" and the actual program that is triggered when you press on the sprint button will appear.

The instruction blocks are actually self explanatory as it is very close to the natural language: When the button is pressed run forward at speed 255 \(which is the maximum\), wait for five seconds \(before proceeding to the next command\) and then stop moving.

Notice there's an event block there about what should happen when the button is released. It is empty, ready for you to put your ideas and orders, there.

![](/assets/Img.2.2.7.jpg)

\[Image 2.9.7: Instructions for the sprint button\]

Let's say, for example, that we'd like to hear a note when the button is released. Click on "~~**Controls**~~" on the toolbar, on the left, and different command blocks should appear. Drag and drop "play a note on ..." just bellow "when button released" taking care that they fit one into the other, like two jigsaw pieces. Then click on the note to pick one of your liking. Eventually add a \(pink\) "wait 1 s" block. You can go to "Play", now, and test your programming. Click on "Sprint" and see if releasing the button will produce a note, as expected. Again, you might want to lift the mBot, so that it doesn't crash on your coffee cup.

Let's make one last improvement. Go back to the Code \(Design &gt; Sprint Button &gt; Code\) and add a "stop moving" instruction block right bellow the "wait 1 s".

Go to "Play" and test the Sprint button, once more. Press "Sprint" and hold your finger there for two seconds and then release it to see if the wheels will stop moving one second after hearing the tone.

The "Buzz" button produces a note when pressed. Edit the instruction so that it produces a C6 note when released, too.

#### More controls

Back to "Design" we can see that there are yet more useful controls that we can add to our mBot. There is, for example, in the "Move" tab a cross-shaped control that we could use, instead of the joystick-like one, to move our mBot.

In tab "Display" we find the "Lightness" button which is interesting to test. Drag and drop it on some empty spot, on the right, and go to "Play" to check it. Moving it left and right should cause the intensity of the LEDs to increase and decrease accordingly.

Back to design mode we find a little piano. If you place it on the canvas and try it out, you will notice that it is not not very responsive. It has quite a bit of a lag between the time that we press on the button and the time that the sound actually comes out of the buzzer.

We can go to the sense menu, too. There you can find items that connect to the sensors that are on board. We've got the ultrasonic in two versions, the numerical and then the gauge with the line graph version and same thing with the brightness, we've got the numerical version and then the line graph version as well.

![](/assets/Img.2.2.8.jpg)

\[Image 2.9.8: The sense menu\]

In the custom menu, you will find all kinds of programmable components.

#### Draw and Run

Another interesting addition in one of the newer versions of this application is the "Draw and Run" option. You can find it back in the begin screen. Clicking on it gives you a canvas in which you can do a little drawing and basically design the path that you would like your mBot to go on. Try, for example, and make a zig-zag route with your finger. When you press "Play", the mBot will try at least to follow the path that you have drawn. Again, take care there's enough space for it. You can experiment with different routes but keep in mind that the path that the mBot actually follows is just an approximation of the path that you have drawn on the path control widget.

![](/assets/Img.2.2.9.jpg)

\[Image 2.9.9: The Draw and Run canvas\]

Most of the components that you can drag and drop on the canvas are pre-programmed, meaning that you don't need to do any programming yourself. If you do want to do a bit of programming, you can use mBlock and we are going to handle this one, next.

### Questions

1. What does the ultrasonic reading mean?

**A. It represents the distance between the ultrasonic sensor and some obstacle.**

B. It represents the amount of light received by the ultrasonic sensor.

C. It represents the amount of light emited by the ultrasonic sensor.

1. Which instruction can stop the moving of the wheels?

A. wait 0 s

B. wait for ever

**C. stop moving**

