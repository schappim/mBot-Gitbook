# Section 6

---

## Chapter 34: Restoring the default program

---

In this chapter you will learn about:

* How to restore the default program
* What is the difference between the "firmware" and the "default program"

---

We saw, in the previous chapter, that the remote control isn't working, after uploading the orignal firmware to the mBot.

Here are the steps that you can follow in order to restore the factory default program so that your remote control can operate again.

1. First, connect the USB cable to the mBot.
2. Then, go to menu Connect &gt; Serial Port and make sure the right serial port is checked, there.
3. Then, go to Connect &gt; Reset Default Program &gt; mBot and an upload process will start, that will last a couple of seconds.
4. When finished unplug the USB

![](/assets/Img.6.34.1.jpg)

\[Image 6.34.1: Step 3: Reseting to the default program\]

If all went well, the mBot should react to the remote control, now. Check it by pressing:

* program A: and watch whether you can direct the mBot using the arrows on the remote control
* program B: and watch whether the line follower sensors react to darkness and brightness.
* program C: and~~** \#\#\#\#\#\#\#\#\#\#\#\#\#NOTSUREWHATITDOES\#\#\#\#\#\#\#\#\#\#\#\#\#**~~

Next, let's click on makeBlock, on the tablet, and see what happens there. Click on the Bluetooth icon on the top right of the screen and you will find that the application is anable to connect to the mBot.

![](/assets/Img.6.34.2.jpg)

\[Image 6.34.2: makeBlock trying to establish connection\]

Notice how the Bluetooth LED on the mBot is solid and that state is actually the reason whey makeBlock cannot connect.

To solve this problem you just need to turn off the mBot and then back again so that the mBot will get into discovering mode, having the Bluetooth LED blinking. Now, makeBlock should be able to connect with it.

![](/assets/Img.6.34.3.jpg)

\[Image 6.34.3: makeBlock establishing connection\]

And that's the difference between the "firmware" and the "default program" options. With "default program" you are able to use your remote control and trigger the three little programs that are stored inside this default program, and in addition you can connect your nBot to your tablet device, and use one of the tablet applications to play around with the mBot.

~~** {{{When with "firmware" happens what exaclty?}}}**~~















