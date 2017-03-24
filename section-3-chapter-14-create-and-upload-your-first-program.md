# Section 3

---

## Chapter 14: Create and upload your first program

---

In this chapter you will learn about:

* 1

* 2

---

We can move on to doing some actual playing around with the mBot using mBlock, now.

On the right bottom corner of the Scripts menu \(1\) you will find the "Robots" section \(2\). Once you select it, there's an mBot section \(3\) which contains all of the different programming blocks that we can use with the mBot.

![](/assets/Img.3.15.1.jpg)

\[Image 2.15.1: The mBot instuction blocks on the Scripts tab\]

Let's have a quick look at some of these instruction blocks.

The first one, for example, reads "run forward at speed 0". Clicking on it, we can change that to backward, right or left, at a particular speed.

There's one that allows us to set the onboard LEDs at a specific colour.

One for taking descisions when the onboard button is pressed and and lots of other blocks for programming behaviour to the mBot.

### Instructions for basic and additional components

Out of the box, the mBot comes with a number of capabilities based on sensors or motors or other attachments like, for example:

* an ultrasonic sensor
* an infrared sensor
* a line follower
* a light intensity sensor

As far as outputs and actuators are concerned, there are:

* two motors connected to two individual ports: one for each motor
* RGB LEDs

Apart from these basic capabilities, though, we can purchase and plug onto the mBot additional components and eventually make use of the mBlock extension to interact with them. So, for example, we can purchase a sound sensor separately and use the correspondive mBlock instuction block to interact with it. A sound sensor is practically a microphone and we can clap, for example, and get the mBot to react to that clapping.

We can have a 3-axis gyroscope, too, which is very good for detecting a change in direction like when the robot turns over, upside-down.

For this crash course on the mBot of course, we will be focusing on the capabilities that the mBot comes with out of the box without any additional components.

### Creating a new program

In order to create a new mBlock program we go to menu "File" and click on "New". In the "Scripts" tab, in "Robots", we pick "mBot Program" and drag and drop it into the scripts area. Every mBot program must start with this header.

Below it, we can attach other compatible blocks. For example, let's say that we would like to change the color of the two onboard RGB LEDs. To do that, we pick the "set led on board..." instruction block and drag and drop it just below the mBot header. Thereafter, we can configure it further by choosing which ones of the two LEDs we would like to manipulate \(left/right/both\) and what colour to set by choosing values from 0 to 255 for all three red/green/blue settings. Through the combination of these three basic colors, we can create all kinds of other composite colors. For our example let's just choose to turn on "all" LEDs and let's pick 255 for red and 0 \(zero\) for the other two basic colours. That should give a plain red colour to both the on-board LEDs.

![](/assets/Img.3.15.2.jpg)

\[Image 2.15.2: A small program that will turn all LEDs to red\]

Once finished with our program we must connect the USB cable to the USB port \(1\) on the mBot. We know that the connection has taken place because there's a red LED \(2\) which indicates that we've got power from the USB. But that's not enough power to power the robot. Once we plug in the cable, we need to turn on the robot by flipping the switch \(3\) to on. Now, the robot is ready to be programmed.

![](/assets/Img.3.15.3.jpg)

\[Image 2.15.3: Connecting the USB on the mBot\]

The next step is to go to the "Connect" menu and look for the serial port where the mBot is connected to the computer by. It's always going to be a port that has a number larger than one. That's because COM1 is typically used by the operating system itself. In our example the port to which the mBot is connected happens to be COM4.

![](/assets/Img.3.15.4.jpg)

\[Image 2.15.4: Connecting to the Serial Port\]

Next, I'm going to do a right click on the mBot program header and choose "Upload to Arduino". Remember how I told you that inside the mBot, you've got an Arduino?

Some people get confused about this, they're saying, "What's the Arduino? I'm trying to program my mBot." It should be saying "Upload to mBot", right? We're saying "Upload to Arduino" because inside the mBot, you have an Arduino. Let's do that "Upload to Arduino". But doing that you've got the uploading component of the mBlock application. What you see here is the translation of the simple scratch-based program into Arduino sketch into Arduino code. The translation is one-to-one. You've got a lot of code here, but most of this code just the infrastructure for supporting the functionality that you've selected in your mBot program.

We want our mBot to just turn the two LEDs into red and this is the block that does that. Everything else that you see here is just in support of that one single thing. In fact, if you have a look inside this line, line 34, you'll see the programming code that actually turns these two LEDs into red. No need to get into the specifics now but this is what causes the LEDs to become red. Everything else is just there to support these two lines of code.

First, you set the color and then you turn the LEDs on with that color. That's all there is. You'll see that as I'm dropping other things, other components, other blocks into my program like this one here, for example, notice that another little instruction was added at the end of my program. If I put it say, up here, notice that the move command now moved at the beginning just before the RGB commands.

The mBlock makes programming easy by providing an interface for us programmers to use a graphical language instead of the traditional text-based language that people are used to using for programming a computer. In any case, as we're just starting now we can completely ignore all these, it makes absolutely no difference to us, you can ignore all that down here as well this part of the user interface. What we need to do is to just click on this button, "Upload to Arduino" just to finish up this whole job. Upload to Arduino, please connect to serial port, I forgot about that.

Again I've got to go back to serial port and choose COM4. Somehow this got disconnected, I'm going to click on "Upload to Arduino" now again. You can see that the uploading has started, there's a lot of texts flowing through. The mBlock application is now compiling the Arduino code using the embedded compiler, compiler is responsible for translating the text into a binary format that the Arduino can understand. I've got upload finish, you can see a nice bright red set of LEDs on the mBot. Let's do this one more time, how about now to make this programming component of mBlock disappear, I just click on "back".

Let's change the LEDs to green. I'm going to make the red component zero and I'm going to make the green component 255. Just like before, I'm going to do a right-click to upload the Arduino, and then again click on the "Upload to Arduino" button. Uploading, verifying and there you go, you've got your two LEDs green. How about I do another Arduino thing, what I'd like to do is to have let's say that right LED to be green and the left one to be blue. I'm going to leave the green here, the green component that's 255 and I'm going to change the LED onboard to be right. I'm going to right-click on the LED block and duplicate it, get another one of those. I will attach it down the bottom of the previous LED onboard block, then I'll change the right LED to left and make the green component zero and the blue component 255.

All the changes that I've just made were automatically inserted in text, the Arduino sketch on the right side. Since I'm already looking at the programming component of the mBlock application, I don't have to go back and redo that, you can see the option to go and upload to the Arduino does not exist here. I can just click on "Upload to the Arduino" button and the upload process will begin.

Here you go, I've got a blue on the right side and a green LED on the left side. How about you try a little variation on this, how about you experiment by creating different colors for each one of the LED. I would like to experiment by combining different values of red, green and blue. Just remember that you're not confined to using those values from the drop-down, you can actually go and change that to an arbitrary value for example 36. To select a color that you like, what you can do is you can use an online color wheel, here's one, for example, you can google for these things this is not the only one.

You can pick a color from the color chooser, let's say you'd like a shade of green, for example, and you can see the values for the red, green and blue component. I would like it to experiment a little bit with this and just create a couple of colors by using this color chooser and getting the mBot IGB LEDs to recreate that color. This will also give you a little bit of practice of uploading a program to the mBot. After that take a break and then we come back from the break, I'm going to show you how to play around with the mortars.

