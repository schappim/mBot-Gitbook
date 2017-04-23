# Section 5

---

## Chapter 26: The line sensor

---

**In this chapter you will learn about:**

* How the line-follower module works
* How to use the line-follower block
* How to program the LEDs to shine according to the line follower status

---

**This chapter contains hands-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will learn about the line module, and how to use it so that your mBot can detect its position relative to a black line.

---

You have learned a lot about your mBot in the previous chapters, but the fun is really starting now.

In this chapter you will play with the line-follower module which is attached to the bottom of the mBot. Even though it behaves as one single unit, it actually contains two sensors, as can be seen in image 5.26.1. These two sensors can detect light intensity \(darkness or lightness\) right in front of them.

![](/assets/Img.5.26.1.jpg)

\[Image 5.26.1: The two light intensity sensors on the line-follower module\]

To prepare for the activities in this chapter, create a line on the floor. The line should be black, around 2cm in width. You can draw yours, or print out the line segments that are provided with this book. Use sticky tape to keep the sheets of paper from moving.

In Image 5.26.2 you can see what such line may look like.

![](/assets/line follower demo 601 2.JPG)

\[Image 5.26.2: An example line that the mBot follows, made of individual line segments\]

Your mBot kit also comes with a fold-out line that you can use right away. It looks like the one in Image 5.26.3.

![](/assets/line follow 2.JPG)

\[Image 5.26.3: This fold-out line comes with your mBot kit\]

Let's start with a little experiment: place the mBot on that dark line and move it a little to the left or to the right so that one of the light intensity sensors is above the line, and the other is not. Notice that there are two tiny indicator LEDs on the module, each one corresponding to one of the sensors. Each of these LEDs is automatically lights up when the corresponding sensor senses brightness underneath, like the white paper, and turned off when there is darkness, which is what it "sees" when it is over the black line \(see Image 5.26.4\).

![](/assets/DSC_0141 600.JPG)

\[Image 5.26.4: The LEDs over each sensor indicate the status of the sensor\]

You can test this by moving the sensor to the left and to the right, relatively to the line.

If both of the sensors happen to be over the white part of the paper, outside the black line, both their LEDs will be turned on. If they are both over the black line, their LEDs will be turned off.

To read the status of the line follower module, you can use the "line follower" block. This block returns the status of the line-follower module in the form of a number, ranging from 0 to 3, with one of the following meanings:

0 = both sensors sense darkness \(they see the black line\) and both indicator LEDs are off.

1 = left sensor senses darkness \(the line\), right sensor senses brightness \(the white paper\); left LED is off, right LED is on.

2 = left sensor senses brightness \(the white paper\), right sensor senses darkness \(the line\); left LED is on, right LED is off.

3 = both sensors sense brightness \(they see the white paper\) and both indicator LEDs are on.

![](/assets/Img.5.26.2.jpg)

\[Image 5.26.5: The "line follower" block\]

Notice that the parameter, in the image above, indicates that the line-follower module is connected on Port 2 of the mBot. If you need to connect it to a different port you should change this parameter accordingly.

You can use this block to determine what it is that the sensor is looking at: whether it is still completely inside the line, completely outside the line, or if one of the two sensors is inside the line and the other one outside it. Depending on this reading, you can program your mBot to react. Your program can direct your mBot to turn a little either to the left or the right, so that both sensors can be repositioned over the line again.

Let's get started towards composing a sketch that can do this. To simplify our work, instead of working with the motors, we can work with the two on-board LEDs. Let's compose a program that uses the LEDs to display the status of the line follower module.  In other words, this program will simply copy the state from the left and right indicator LEDs of the line follower module to the  two big RGB LEDs of the mBot.

Create a new project and compose the program that you can see in Image 5.26.6.

![](/assets/Img.5.26.3.jpg)

\[Image 5.26.6: The program that copies the status of the sensors to the LEDs of the mBot\]

Here's what happens in this program:

Notice that there is a variable named "line\_sensor\_status".

First the program reads the status of the line follower module and stores it to variable "line\_sensor\_status".

Then it checks the value of this variable. As you know, this value can be either 0, 1, 2 or 3. If the value stored in "line\_sensor\_status" is 0 \(meaning that both sensors are on the black line\), then the program will turn both LEDs off.

Else, if the value is 1 \(meaning that the right sensor sees the white paper\), then the program will turn the right LED on.

Else, if the value is 2 \(meaning that the left sensor sees the white paper\), then the program will turn the left LED on.

Else, the only other option for the value is for it to be 3 \(meaning that both sensors see the white paper\), so the program will turn both LEDs on.

The program will repeat this process forever.

Go ahead to upload this program to your mBot and test it. When the program is uploaded, position your mBot on the black line so that both sensors are on it. Experiment by moving each and both sensor over the line and outside the line. You should notice that the LEDs turn on and off accordingly, indicating what it is that the two sensors see: the black line or the white paper.

And since you have done all this interesting work, don't forget to save the program with the name "Line sensor with LEDs".

In the next chapter, you will add Scratch blocks to control the motors the motors so that your mBot moves on the line by constantly checking its position with the line follower module, and makes small adjustments when it detects that it is about to exit the line.

---

### Question 5.26.1: How many different statuses does the line follower have?

A. None

B. Three

C. Four

D. It depends on the port, where the sensor is connected.

_Answer: C_

---

### Question 5.26.2: What does the "line follower" Scratch block actually do?

A. It evaluates to either true or false, depending on the line follower reading.

B. It returns the status of the line -follower module as a number.

C. It returns the number of the port where the line follower is connected.

D. It sends directions to the line-follower.

_Answer: B_

---

**Checklist**

Double-check that at this point, the following are completed:

\[   \] You understand the principle of operation of the line follower module

\[   \] You understand the role of each of the line follower sensors that make up the line follower module

\[   \] You know how to use the Scratch "line follower" block 



