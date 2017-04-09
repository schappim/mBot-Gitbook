# Section 6

---

## Chapter 33: Restoring the firmware

---

At this point, we spent quite a bit of time programming the mBot using mBlock. Let's make an experiment, now.

To begin with, let's have some program executing on the mBot. And let's say that we would like to experiment further with the mBot using one of the three applications we have seen at the beginning of the course, on the tablet.

With the mBot turned on we will notice that the Bluetooth module is blinking, which means it is in discovery mode.

Let's start now the Makeblock application and try to connect the mBot to the tablet by clicking on the Bluetooth icon, on the top right of the screen. We will notice that the Bluetooth LED is solid now, indicating that there is a connection, but we will get the error message: "Device Dismatch - Robot may behave incorrectly, Connect Another Device" followed by the one shown in the picture below:

![](/assets/Img.6.33.1.jpg)

\[Image 6.33.1: The conectivity error message\]

This means that even though there is a connection between the mBot and the tablet, the latter is not able to send instructions to the mBot because of our software running on the mBot. Makeblock needs the original firmware, to interact with the mBot, but finds our software there, instead.

A second thing that the mBot is unable to do, right now, is to be controled by the remote control. If we pick it and press the buttons on it, nothing will happen.

Another thing that has changed is that the default factory programs, that the mBot came with, are also not there anymore because they have been overridden by our program.

To restore the factory firmware with all the original functionality, we can follow these steps:

* Connect the mBot to the computer via USB.
* Connect the serial port via menu: Connect &gt; Serial Port &gt; ...
* Check to make sure that the mBot is checked in menu Boards
* Restore the original firmware by going to Connect &gt; Upgrade Firmware

Once clicked the firmware will start uploading like this:

![](/assets/Img.6.33.2.jpg)

\[Image 6.33.2: Uploading the firmware\]

When the upload is finished we go on like this

* Turn the mBot off and then back on again.
* Disconnect the USB from the computer.
* 






\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\# I can use the mBlock application on my computer and I'm going to show you how to do that now.

First, let's say that I'd like to restore the firmware so that I can play with my mBot using my iPad. The way to do that is to start up my mBlock application. I need to connect my mBot to my computer via USB. It's done. I'm going to connect the serial port. Right now, this is a serial port that my mBot is connected to my Mac, so we choose that. Usually bots are okay by default so import the mCore controller, it's all set. Then all I’ve got to do is to upgrade firmware, so click on that and then the upgrade starts.

\[pause\]

And upload finish so now let’s try again. I'm going to turn the mBot off and then back on again. Just remove things bit closer to my overhead camera. All right. That's better. I can remove the cable now from the computer. I don't need it anymore. I'll turn it on. The mBot is now connected. Let’s see. Connected automatically, that’s happened actually really quickly, surprisingly.

Just because the application was running already on my iPad, as soon as the mBot went back to life, the Bluetooth module connected the mBot to my iPad. Now, I can interact with it. There you go. It works. I just lifted to do the sprint. \[background noise\] There you go.

Back to normal. All right. That is great. Let’s see if my remote control works now. No, the remote control isn't working.

Let me show you what to do in order to restore the factory default program so that your remote control can operate again.

