# Section 6

---

## Chapter 33: Restoring the firmware

---

**In this chapter you will learn about:**

* How to restore the original firmware so that you can use your mBot with your iPad or Android tablet

---

Let's start this chapter with an experiment.

Start by uploading the last version of the line following program to your mBot. Next, take your tablet, start Makeblock, and try to connect your mBot as described in Chapter 9.

With the mBot turned on, confirm that the Bluetooth module indicator LED is blinking. This means that the module is in discovery mode.

Start the Makeblock application on your tablet and try to connect it to the mBot by clicking on the Bluetooth icon, on the top right of the screen \(please see Chapter 9 for the detailed instructions on how to connect the two devices\).

Notice that the Bluetooth indicator LED is now solid, suggesting that there is a connection, however you will get the error message: "Device Mismatch - Robot may behave incorrectly, Connect Another Device" followed by the one shown in Image 6.33.1.

![](/assets/Img.6.33.1.jpg)

\[Image 6.33.1: The connectivity error message\]

This means that even though there is a connection between the mBot and the tablet, the latter is not able to send instructions to the mBot because the line following program is still on your mBot.

For your tablet to be able to communicate with your mBot, the mBot must be have a special program, that for the purposes of this chapter we can call "firmware".

A second thing that the mBot is unable to do, right now, is to be controlled by the remote control. If you pick it and press the buttons on it, nothing will happen. Remember that back in Chapter 5, you were able to control your mBot with the provided infrared remote controller. This capability is made possible by another special program, which we call the "default program".

Here is how to restore the original firmware so that you can control your mBot with your tablet:

1. Connect the mBot to your computer via USB.
2. Connect the serial port via menu: Connect &gt; Serial Port &gt; ...
3. Check to make sure that the mBot is checked in menu Boards
4. Restore the original firmware by going to Connect &gt; Upgrade Firmware \(see Image 6.33.2\)

![](/assets/mbot 270 280 Screen-00-03-29-446.png)

\[Image 6.33.2: Click "Upgrade Firmware" to upload the firmware \(program\) to your mBot\]

Once clicked the firmware will start uploading \(your can see the progress status box in Image 6.33.3\).

![](/assets/mbot 270 280 Screen-00-03-40-205.png)

\[Image 6.33.3: Uploading the firmware\]

When the upload is finished, continue by:

1. Disconnect the mBot from your computer.
2. Turn the mBot off and then back on again in order for the newly uploaded firmware to start running \(executing\) on your mBot.

The Bluetooth LED should appear solid now. If it isn't you should click on the Bluetooth icon, on the top right corner of the screen.

Your mBot is now connected to your tablet \(Image 6.33.4\)!

![](/assets/Img.6.33.3.jpg)

\[Image 6.33.4: The mBot "Connected" message\]

If you click now, on buttons "Sprint" and "Buzz", the mBot should react by sprinting the wheels and making a beep, respectively.

If you check the remote control, though, nothing will happen. That's because the remote functionality is implemented by a special program. This is the program that was in your mBot when it came out of the box. Not only it implements the remote control functionality, with the three demonstration programs that you learned about in Chapter 5, but it also makes it possible to connect your mBot to your tablet so that you can use it with applications like mBlockly and MakeBlock. This is the "all in one" program! In the next chapter you will learn how to restore the factory default program so that the remote control can operate again.

---

Question 6.33.1: What might be the cause of an "Unrecognizable Firmware" error?

A. The USB is not connected to the mBot.

B. The wrong COM port is checked.

C. A custom program has replaced the factory software.

D. At least one variable name cannot be recognised by the mBot.

_Answer: C_

---

Question 6.33.2: What functionality is implemented by the firmware?

A. Blinking RGB LED demo program

B. Line following demo program

C. Ability to connect the mBot to a tablet

D. All of the above

_Answer: C_

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] You know how to restore the firmware on your mBot

\[   \] You know the functionality implemented by the firmware

\[   \] You know the difference between the functionalities implemented by the firmware, and the default program





