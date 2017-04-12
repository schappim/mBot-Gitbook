# Section 3

---

## Chapter 16: Motor control

---

In this chapter you will learn about:

* How to program the mBot to move forwards
* How to control the speed of your mBot
* How to reset your mBot

---

**This chapter contains hand-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will compose your first mBot sketch and learn how to upload it to your mBot.

---

In the last chapter you learned how to get the two LEDs to display two different colours. In this chapter, you are going to learn how to use the two motors.

Each mBot comes with two motors.

They are connected to the dedicated Motor ports, marked "M1" and "M2", as you can see in Image 2.16.1.

![](/assets/Img.3.16.1.jpg)

\[Image 2.16.1: The two motor connectors\]

Go ahead and create a new program in mBlock. You will compose this program in order to play with the motors. As you learned in the previous chapter, to create a new program, go to menu "File" and click on "New".

Start composing your program by dragging the "mBot program" block from the blocks palette.

There are a couple of different blocks that allow you to control the motors. Start with block "\[run forward\] at speed \[0\]" which allows us to get the mBot to move forwards or backwards and turn left or right \(see Image 2.16.2\).

Pick it and attach it to the "mBot program" header block and then continue by configuring its two attributes:

a. the direction of the move

b. the speed

![](/assets/2017-04-12_13-00-50.png)

\[Image 2.16.2: The "run forward" block takes two parameters\]

The speed can take any number between -255 and 255. Again, instead of selecting one of the values from the drop-down, you can click and enter any valid value. A negative value here will have the robot run backwards \(with the direction attribute set to "run forward\]\) and vice versa. Let's choose "forward" and a speed of 125.

---

### BEWARE!

The speed parameter number is rather arbitrary and how fast the robot goes really depends on how depleted are the batteries or whether there is some load on the robot.

---

Let's add a "wait" block and set it to 5 seconds. Following that, add another "run forward" block and set it at a speed zero, which will stop the spinning of the wheels.

![](/assets/Img.3.16.2.jpg)

\[Image 2.16.3: The described Scratch blocks and the corresponding Arduino text\]

Great, your motor test program is ready!

Right click, now, on the "mBot program" block and select "upload to arduino". Then, click on "Upload to Arduino" to upload the program to your mBot. You should make sure first, of course, that you the mBot is connected to the appropriate COM port, like we saw in the previous chapter.

---

#### PRO TIP:

If you are working on a table with limited space and don't want your mBot to fall of the table or knock your things around, it is a good idea to hold the mBot up or place it upside-down so that its wheels are free to spin.

---

After uploading the program you will see the wheels spinning for 5 seconds and then stop.

In order to test the robot on the floor you should turn the switch off, unplug the USB cable and and place it on the floor with sufficient space for it to move forward..

The mBot is powered by the batteries and the program is always stored inside the Arduino board even though you turned it off. When you turn the mBot back on, it will execute it the stored program automatically, but only once.

There are two ways to execute the program again:

1. by powering cycle the mBot: turning it off and then back on.
2. by pressing the Reset button on the mBot The Reset button is next to the USB port, and you will need a pointy object to press it.

In the next chapter you will learn how to program the mBot to turn left, right and then move backwards, as well.

---

#### Question 3.16.1: What will be the effect of this command: "run backward at speed -100"

A. It will have the mBot move forwards

B. It will have the mBot move backwards

C. It will have the mBot stop

D. It will return an error

_Answer: A_

---

#### Question 3.16.2: How can we run again a program that is stored in your mBot?

A. By creating a new program

B. By clicking on the reset button, on the mBot

C. By turning off the mBot, and then back on

D. Both B and C

_Answer: D_

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] You know how program your mBot to move forwards and backwards

\[   \] You know how to program your mBot to move at different speeds

\[   \] You know how to program your mBot to stop moving

\[   \] You know how to reset your mBot

