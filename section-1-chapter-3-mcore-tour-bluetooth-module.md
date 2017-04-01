# Section 1

---

## Chapter 3: Assembly: mCore tour and Bluetooth module

---

**In this chapter, you will learn about:**

* The different components on the mCore board
* How to connect the Bluetooth module

---

**This is a hand-on activity.**

No tools are necessary. You will need the mCore and the Bluetooth module.

---

In this chapter you will work with the mCore, the microcontroller module.

Remove the protective film from the bottom of the mCore as there is no need for it any more. The first thing to do is to gently open up the case. Hold the top and bottom plastic cover in your hands, and carefully pull them away from each other. They should come off easily as there are no screws holding them in place.

![](/assets/Img.2.3.1.mCore.jpg)

\[Img 1.3.1: The mCore layout\]

Take a few minutes to become familiar with the parts that make up this module. Here they are \(use Image 1.3.1 as reference\):

### 1

The small square integrated circuit in the middle is the ATmega328/P microcontroller. This is the brain of the mBot. It’s the same microcontroller that you find on the Arduino UNO.

### 2

a. The infrared receiver

b. The infrared transmitter.

With the infrared receiver, we are able to use the remote controller \(the one that comes with the mBot\) and get it to move in particular directions. We can program the mBot so that it performs a particular behaviour when a button of the remote controller is pressed. For example, we can program key "0" to play a tone, and button "1" to make the mBot spin. With the transmitter, on the other hand, we can get the mBot to transmit infrared signals to other mBots.

### 3

There is a buzzer, so that the mBot can make noises.

### 4

There are two RGB colour LEDs, each capable of producing thousands of colours.

### 5

In between the RGB LEDs is a light sensor which is used by the mBot to figure out whether it is day or night, whether a light is turned on or off, or whether there is light or darkness.

### 6

There's a general purpose button that can be programmed to do things like making a noise, starting the motor, etc.

### 7

There's a reset button that resets the program on the mBot.

### 8

There are four numbered connectors \(one, two, three, and four\) where you can plug in the various modules. The range finder or the light follower sensor, for example, can connect to any one of those sockets.

### 9

These are the connectors where we plug the DC motors.

### 10

The on-off switch.

### 11

The LiPo battery connector. Next to the LiPo connected you will find a black barrel connector. You will use this connector to connect the AA battery holder. This is the main power source for your mBot.

### 12

The is a USB connector. You will use this connector to connect the mBot to your computer and upload a program. It is exactly the same connector that you find on an Arduino UNO.

### 13

The connector for the communications module. The mBot operates with two different modules. One is just the radio frequency module and the other one is a Bluetooth module. In our case, we'll be using the Bluetooth module, which is very easy to connect: just align it, plug it in and you've got it connected.

---

**Attention:** One troublesome design issue that is the cause of many headaches is that you can actually plug the Bluetooth module in reverse. It will still fit in the socket just fine, and you will be able to attach the cover of the mCore just fine. It will connect but of course it is not going to work because it's plugged in the wrong way. I've seen this happening in large groups of people where mistakenly somebody will just plug in the module, then put the cover back on, continue with the assembly of the mBot, and then half an hour later, the thing isn't working and that's because the module was plugged in the wrong way. So be very careful here.

---

Notice that the antenna design is printed clearly on both the module and the mBot controller board. That's a hint that you can give your students, that they have to align the printed shape of the antenna on the module with the one on the mBot controller board, and of course the pins should also match precisely.

In order to finish, put the cover back on, applying a little bit of pressure, so that the clips connect.

---

**Question 3.1: Can you think of three things that you can get your mBot to do with the buzzer? Write them down!**

1 \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

2 \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

3 \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

_Answer: Things like \(1\) a beep to tell you that a program has finished its operation, \(2\) a beep to tell you that it has detected an obstacle, \(3\) play music, \(4\) an audible greeting when a program starts, \(5\) a beep when you press the button._

---

**Question 3.2: How many colours can you create with the onboard RGB LEDs?**

A. One

B. 256

C. 1000

D. Many thousands

_Answer: D_

---

**Question 3.3: How many motors can you connect directly to the mCore?**

A. One

B. Two

C. Three

D. Four

_Answer: B_

---

**Question 3.4: As you know, the mCore has an infrared receiver and transmitter onboard. This means that it can communicate with other mBots, and that you can control it with the supplied infrared remote controller. Think about a game that involves two mBots, communicating with each other. Can you come up with the rules and the objective of such game?**

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

_Answer: This is an open-ended question. There is no assumption or expectation of a particular game that we want the students to come up with._

---

**Checklist**

Double-check that at this point, the following are completed:

\[    \] The Bluetooth module is properly attached to the mCore, with its antenna pointing towards the back

\[    \] The top cover of the mCore board is properly attached to the bottom cover

---



