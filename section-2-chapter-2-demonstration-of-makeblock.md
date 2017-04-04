# Section 2

---

## Chapter 9: Demonstration of the MakeBlock

---

**In this chapter you will learn about:**

* What is Makeblock
* What you can you do with Makeblock
* How to connect your mBot to MakeBlock
* How to use the various widgets to control your mBot
* How to use the various widgets to receive sensor data from your mBot and visualise it

---

**This chapter contains hand-on activities.**

You will not need any tools.

You will need your mBot and an iPad tablet computer with the MakeBlock application installed.

![](/assets/2017-04-04_16-45-01.png)

Get MakeBlock from the Apple App Store \(for iOS devices\) or the Play Google Store \(for Android devices\). Find a download link at learn.makeblock.com/en/software/

---

### Makeblock

By using the Makeblock app you can control your mBot without doing any programming at all. When you start the application, you see a lot of pre-existing apps that you can play with right away, instead of spending time programming the mBot.

This way, you can explore the various features and capabilities of the mBot right away.

After starting the app you see a variety of mBot configurations. The simplest of them, and the one you should start with is called _mBot_.

---

**BEWARE!**

In MakeBlock, applications that are tagged with "M+" need an mBot with additional attached components.

For example, there's one that requires the six-legged robot extension components, in addition to the mBot. There's another one that requires a different kind of motor, called a "servo", as well as mechanical extension rods. These are available as a seperate kit.

---

![](/assets/makebot1.png)

\[Image 2.9.1: The begin screen\]

Let's start with the basic mBot app, at the top left. Once the app starts, you will see a set of controls:

1. A joystick for controlling the two DC motors. 
2. numerical reading of the distance between the sensor and an object in front of it
3. A line chart display of the light sensor readings
4. on/off switch that will get the robot to execute a random movement
5. A button that will activate the buzzer and make some noise
6. A button  button that will make the robot to move forwards at maximum speed

![](/assets/Img.2.2.2.jpg)

\[Image 2.9.2: The controls\]

Tapping on the "Design" tab reveals all the components that can be dragged and dropped onto the canvas. These components are sorted under four categories:

1. Move
2. Display
3. Sense
4. Custom

![](/assets/design.png)

\[Image 2.9.3: Additional controls on the Design tab\]

Before going any further you should first connect your mBot to the iPad. Let's do that now.

#### Connecting the mBot to the iPad

Turn the mBot on if it isn't on already. If your mBot is already turned on, and connected to another device via Bluetooth, the easiest way to reset it is to turn it off and then back on again. Doing this will drop the original Bluetooth connection, and make your mBot available to connect to another device or application.

With this done, you should see a blue light blinking on the top of the mCore controller, near the power plug. This indicates that the Bluetooth module is available to be paired \(connected\) to a Bluetooth device. That can be your smartphone, your tablet or your desktop computer, if it has got a Bluetooth module integrated.

![](/assets/Img.2.2.4.jpg)

\[Image 2.9.4: The Bluetooth icon\]

In your device, tap onto the Bluetooth icon that is blinking on the top right corner of the screen. That will get the app to start searching for a nearby mBot. In case you see the message "Device found, please get closer", just get the mBot a little closer to the device.

And that is all it takes to complete the connection between the app and the mBot!

#### Trying out the different controls

Now you can go ahead and make your first attempt to control something on the mBot.

How about trying to change the colour of the LEDs on the mBot? Touch the colour wheel and try changing the RGB LED colors. Touching on the red, or the blue, for example, will make the mBot LEDs to turn red and blue.

![](/assets/Mbot - 0080 - Ipad 1 - demo of Makeblock mblockly mblock.CONSTANT-00-06-23-598.png)

\[Image 2.9.5: The colour wheel\]

Next, you can try the ultrasonic sensor gauge. Put your hand, or some other object, like a book, in front of the sensor and slowly move it closer to the sensor and you should be able to see the ultrasonic reading, in the app, changing \(see Image 2.9.6\).

![](/assets/Mbot - 0080 - Ipad 1 - demo of Makeblock mblockly mblock.CONSTANT-00-06-43-682.png)

\[Image 2.9.6: The ultrasonic distance indicator shows distance in centimetres. The brightness chart show light intensity from 0 \(dark\) to 1023 \(very bright\)\]

Next, let's play with the light sensor. Use your palm to cover the top of the mBot, where the sensor is located. You should see that the corresponding reading in the app increases \(see example in Image 2.9.7\).

---

**BEWARE!**

Remember to turn off the LEDs on the mBot first, for better results. If you don't, the light they produce will be detected by the sensor, probably causing the brightness line in the cart to fluctuate. You can always turn the LEDs on and off by going to Design Mode \(just click on "Design" on the top of your screen\).

---

![](/assets/Img.2.2.6.jpg)

\[Image 2.9.7: Covering the light sensor with the hand\]

Obscuring the light sensor will make the yellow line in the brightness chart to go lower. The numbers you see on the left are not particular light measuring units but rather an analogue input number of the mBot: when the mBot is connected to an analogue device, like the light sensor, it produces a number that represents the the value that the sensor is measuring. In the case of the light sensor on the mBot, light of low intensity is represented by a small number in the chart. Light of higher intensity is represented by a larger number in the chart.

How about you make some noise now? Tap on the button labeled "Buzz". Can you hear the noise?

![](/assets/Mbot - 0080 - Ipad 1 - demo of Makeblock mblockly mblock.CONSTANT-00-06-43-682 %280%29.png)

\[Image 2.9.8: With the joystick you can control the movement of your mBot\]

Next we can try and control the mBot. The control lever is very much like a joystick \(see image 2.9.8\). Try all different directions with it and you should see the mBot react accordingly.

Before testing the sprint button make enough space for the mBot to run. You can always lift it up in the air, before it smashes on anything. Keep in mind that the sprint can be reset by using the joystick.

Last, try out the "Random" switch. Switching "Random" on will produce a random effect on the mBot like turning the LEDs on etc.

#### The program behind the controls

In MakeBlock, when you press a button or turn on a switch, the action that is triggered is defined by a program that is hiding behind the button. 

Are you curious to find out what these programs look like? Sure you are!

To have a look at the mechanics behind the controls go back to "Design" tab. Let's find out how the Sprint button works. Tap on it and in the menu that opens choose "Code" and the actual program that is triggered when you press on the sprint button will appear.

![](/assets/Mbot - 0080 - Ipad 1 - demo of Makeblock mblockly mblock.CONSTANT-00-12-02-966.png)

\[Image 2.9.9: While in Design mode, tapping on a button reveals the options menu. Tap on Code to see the code behind a button\]

There are two instruction blocks behind the Sprint button. One contains code that controls the mBot when the button is pressed, and the other when the button is released. The first time you look at the Sprint code, there should not be any code under the "when button released" block.

Under the "when button pressed" block, there are three instructions which should be easy for you to understand the purpose of. 

The first one tells the mBot to move forwards at speed 255. 

The second one tells the mBot to continue doing that \(moving forward at speed 255\) wait for five seconds.

The third one tells the mBot to stop moving.

---

**BEWARE!**

For the mBot, the value "255" describes the maximum possible speed that its motors can spin at. 

Value "0" translates to the motors being stopped.

---

![](/assets/Mbot - 0080 - Ipad 1 - demo of Makeblock mblockly mblock.CONSTANT-00-12-08-196.png)

\[Image 2.9.10: Instructions for the sprint button\]

How about we add some instructions under the "when button released" block?

Let's say, for example, that we'd like to hear a note when the button is released. Tap on "Controls" on the toolbar, on the left, and different command blocks should appear. Drag and drop "play a note on ..." just below "when button released" taking care that they fit one into the other, like two jigsaw pieces. Then tap on the note to pick one of your liking. Eventually add a \(pink\) "wait 1 s" block from the Controls category. You can go to "Play", now, and test your programming. Tap on "Sprint" and see if releasing the button will produce a note, as expected \(see Image 2.9.11 for some hints on the layout of the Design screen as you are putting together your program, and Image 2.9.12 for the final set of instructions under "when button release"\). 

You might want to lift the mBot, so that it doesn't run of your table.

![](/assets/Mbot - 0080 - Ipad 1 - demo of Makeblock mblockly mblock.CONSTANT-00-12-37-970.png)

\[Image 2.9.11: Drag the "play not on C5" block and attach it to the "when button released" block\]

![](/assets/Mbot - 0080 - Ipad 1 - demo of Makeblock mblockly mblock.CONSTANT-00-12-56-169.png)

\[Image 2.9.12: The final set of instructions for the Sprint button\]

Let's make one last improvement. While still in Design mode, add the "stop moving" block from the Move category right under the "wait 1 s" block in the "when button released" block. This way, when you release the Sprint button, the mBot will first make a noise, and then it will stop moving.

Go back to "Play" mode and test the Sprint button, once more. Press "Sprint" and hold your finger there for two seconds and then release it to see if the wheels will stop moving one second after hearing the tone.

The "Buzz" button produces a note when pressed. How about you edit the instruction so that it produces a C6 note when released, too.

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

Question 2.9.1: What does the ultrasonic reading mean?

A. It represents the distance between the ultrasonic sensor and some obstacle.

B. It represents the amount of light received by the ultrasonic sensor.

C. It represents the amount of light emitted by the ultrasonic sensor.

Answer: A

Question 2.9.2: Which instruction can stop the moving of the wheels?

A. wait 0 s

B. wait for ever

C. stop moving

Answer: C

