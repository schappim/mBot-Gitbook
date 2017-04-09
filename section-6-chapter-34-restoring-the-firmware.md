# Section 6

---

## Chapter 33: Restoring the firmware

---

At this point, we spent quite a bit of time programming the mBot using mBlock. Let's make an experiment, now.

To begin with, let's have some program executing on the mBot. And let's say that we would like to experiment further with the mBot using one of the three applications we have seen at the beginning of the course, on the tablet.

With the mBot turned on we will notice that the Bluetooth module is blinking, which means it is in discovery mode.

Let's start now the Makeblock application and try to connect the mBot to the tablet by clicking on the Bluetooth icon, on the top right of the screen. We will notice that the Bluetooth LED is solid now, indicating that there is a connection, but we will get the error message: "Device Dismatch - Robot may behave incorrectly, Connect Another Device" followed by the one shown in the picture below:

![](/assets/Img.6.33.1.jpg)

\[Image 6.33.1: The connectivity error message\]

This means that even though there is a connection between the mBot and the tablet, the latter is not able to send instructions to the mBot because of our software running on the mBot. Makeblock needs the original firmware, to interact with the mBot, but finds our software there, instead.

A second thing that the mBot is unable to do, right now, is to be controlled by the remote control. If we pick it and press the buttons on it, nothing will happen.

Another thing that has changed is that the default factory programs, that the mBot came with, are also not there anymore because they have been overridden by our program.

To restore the factory firmware with all the original functionality, we can follow these steps:

* Connect the mBot to the computer via USB.
* Connect the serial port via menu: Connect &gt; Serial Port &gt; ...
* Check to make sure that the mBot is checked in menu Boards
* Restore the original firmware by going to Connect &gt; Upgrade Firmware

Once clicked the firmware will start uploading like this:

![](/assets/Img.6.33.2.jpg)

\[Image 6.33.2: Uploading the firmware\]

When the upload is finished we go on like this:

* Disconnect the USB from the computer.
* Turn the mBot off and then back on again.

The Bluetooth LED should appear solid now and Makeblock might connect automatically. If it doesn't we should click on the Bluetooth icon, on the top right corner of the screen.

![](/assets/Img.6.33.3.jpg)

\[Image 6.33.3: The mBot "Connected" message\]

If we click on buttons "Sprint" and "Buzz", now, the mBot should react by sprinting the wheels and making a beep, respectively.

If we check the remote control, though, nothing much will happen and next we will see what to do in order to restore the factory default program so that the remote control can operate again.

### Questions

Question 6.33.1: What might be the cause of an "Unrecognizable Firmware" error?

A. The USB is not connected to the mBot.

B. The wrong COM port is checked.

C. A custom program has replaced the factory software.

D. At least on variable name cannot be recognized by the mBot.

_Answer: C_

