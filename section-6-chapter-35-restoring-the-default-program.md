# Section 6

---

## Chapter 34: Restoring the default program

---

In this chapter you will learn about:

* How to \#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

---

We saw, in the previous chapter, that the remote control isn't working, after uploading the orignal firmware to the mBot.

Here are the steps that you can follow in order to restore the factory default program so that your remote control can operate again.

* First, connect the USB cable to the mBot.
* Then, go to menu Connect &gt; Serial Port and make sure the right serial port is checked, there.
* Then, go to Connect &gt; Reset Default Program &gt; mBot

and an upload process will start, that will last a couple of seconds.

![](/assets/Img.6.34.1.jpg)

\[Image 6.34.1: Reseting to the default program\]

and then back to N block, and go back to connect, make sure that you've got the correct serial port selected. Okay, it is, I heard a little beep. Then to reset the default program we just select "reset default program for the NBot." We choose that, and we'll start uploading the default program, and get out of the makeblock application on the IPad as well.

\[beeping noises\] Okay, so that's done. Unplug the USB and here's my remote control. Let's see, does it work? I'll select program A. All right, there's the response. Yes, it works. I don't have a line to follow, but program B should also work. \[beeping noise\] You can see that if I move my fingers across the sensors for the light sensor, the NBot responds.

All right. thats good, and what about program C? Yes, program C also works. All right, back to A. Now, let's see. Can we also use the default program to connect to one of the tablet applications so I'll go back to make block.

The blue LED on the Bluetooth model is solid, so it's trying to find a net block device. It's not able to find it because of the state of the Bluetooth module, so I'm going to try to turn off nCore and turn it back on. Go back to get my Bluetooth module back into discovering mode. You can see that the device found now can be closer and connected. There we go. That's the difference between firmware option and the default program option. With the default program option you are able to use your remote control and trigger the three little programs that are stored inside this default program, but you can also use it to connect your nBot to your tablet device, and use one of the tablet applications to play around with your NBot.

