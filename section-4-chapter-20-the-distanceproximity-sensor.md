# Section 4

---

## Chapter 21: The distance/proximity sensor

---

**In this chapter you will learn about:**

* How to use the distance/proximity sensor
* How to program the distance/proximity sensor

---

**This chapter contains hands-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will learn about the proximity sensor and use it to allow your mBot to detect objects.

---

In the previous chapter you learned to use the "forever" loop block, and wrote a program that makes the two onboard RGB LEDs to blissfully blink forever. Let's move on now, and learn about the proximity sensor.

### Operation of a distance/proximity sensor

The proximity sensor measures the distance between the mBot and an object in front of it. The sensor works well at distances up to 30 or 40 centimetres. The measurement accuracy depends on the shape and material of the object. 

The sensor works by emitting an ultrasound, which is a high-pitched sound that humans can't hear. Other animals, like bats, do, and use ultrasounds to navigate in space. The sensor will emit a short-duration ultrasonic "ping" of a few milliseconds in duration. The sounds will travel until it reaches an object. Then, it will bounce on the object and, at least part of it, will travel back to the sensor. The receiver on the sensor will pick up the echo, and using the total time it took for the original sound to travel to the object and return, it will calculate the distance of the object.

For the distance calculation to be accurate, the surface of the object must be reflective and large enough for the ultrasonic ping to return to the sensor with enough power. Small objects, or objects that absorb sound will not reflect enough sound, so the reading from the sensor will not be accurate. 

The further away you go from the object, the larger the object has to be in order for the sensor to pick up the distance correctly. You will find, for example, that a pen might be too small for the sensor to be able to detect and to measure its distance. A larger object with a flat surface, like a book, makes a better target for this kind of sensor. The principle of operation is the same by which a sonar works for a submarine. 

The sensor contains two main components:

* the **transmitter**, which emits a ping: an ultrasonic sound which is going to reach the object, bounce off it and then come back.
* the **receiver**, which listens out for those bounced signals.

Internally the sensor will calculate the amount of time that it takes for the signal to travel to the obstacle and then to come back. From that information, it will work out the distance in centimetres or inches or any other measuring unit you can control.

---

#### Question 4.21.1: What is the range of frequencies of sound that are considered "ultrasonic"? Search Wikipedia for the answer.

A. Between 20 kHz and 30 kHz

B. Above 40 kHz

C. Between 20 kHz and 40 kHz

D. Anything above 20 kHz

Answer: D \(from https://en.wikipedia.org/wiki/Ultrasound\)

---

#### Question 2.21.2: What is the top end sound frequency that a dog can hear?

A. 20 kHz

B. 45 kHz

C. 64 kHz

D. 160 kHz

Answer: B \(from https://en.wikipedia.org/wiki/Ultrasound\#Animals\)

---

### Programming the sensor

Go ahead and create a new project in order to see how the ultrasonic distance sensor works \(in the mBlock menu click on File and then New\).

As always, start by placing the mBot program header block in the program area. Next, drag and drop an "ultrasonic sensor \[Port3\] distance" on the canvas. 

Remember to set the port for the ultrasonic sensor block to the port that you have connected the sensor to your mBot's mCore controller.

Notice that this block lacks the indentation that allows it to connect to the mBot program header block.

Blocks with rounded corners, like this one, are meant to return a value. One way to use such a block is to place it within a "set variable" block, assigning the returned value to some variable.

Let's create, therefore, a new variable. In the Data&Blocks group of blocks, click on "Make Variable" and give it the name "distance".

Next step, drag the "set \[distance\] to ..." block and attach it below the header bock. And now you can move the "ultrasonic sensor \[Port3\] distance" block and make it the second attribute in "set \[distance\] to ..." like shown in the image below:

![](/assets/Img.4.21.1.jpg)

\[Image 4.21.1: Assigning the ultrasonic sensor reading to variable "distance"\]

If your ultrasonic sensor is connected to some other port than Port3, you need to change this attribute accordingly.

Next, add a "set led on board ..." block, attach it to the program and place variable "distance" in all the three attribute spots:

![](/assets/Img.4.21.2.jpg)

\[Image 4.21.2: Setting the LEDs to emit a quantity of light corresponding to the distance from the object\]

Τhe problem, here, is that these two instruction blocks will only execute once and then the program will stop. If you upload and execute this program, you will see that it will get just one single measurement with the sensor and then finish, which is not what we want. 

In most cases where a sensor is involved, you want to take measurements repeatedly, and as quickly as possible, because you want your robot to continue sensing changes in the environment. In order to have these two instructions execute repeatedly you need to place them within a loop. 

So, go ahead and add a "forever" loop block, and arrange the blocks by moving them around, to achieve the order shown here below:

![](/assets/Img.4.21.3.jpg)

\[Image 4.21.3: The final program\]

---

**Did you know**

The colour of the blocks depends on the block group to which it belongs.

---

Can you figure out what is it that this program will do when you upload it to your mBot?

As the distance from the object increases, the brightness of the LEDs will decrease. As the distance from the object decreases, the brightness will increase accordingly. Now that your program is complete you can test it in practice.

Make sure that you've got the right COM port connected and then "Upload to Arduino".

Place some object in front of the sensor, like a book, and then slowly move it closer to the sensor and back again. Notice that the intensity of the LEDs grows stronger or fainter, depending on the distance between the object and the sensor.

When there is no object ahead of the mBot, or when the object is too close to the sensor, you will notice that the LEDs will be at the brightest setting. The reason for this is that in both cases there can be no reading. The signal either doesn't return or, when we are too close, there is just not enough space for the signal to travel from the transmitter to the object and back to the receiver.

---

#### Question 2.21.3: With the last version of the program running on your mBot, experiment with various objects and materials. Look on your desk and try things like a pencil, a sheet of paper, some thick fabric. Which one of the objects seems to work best with the ultrasonic sensor? Can you explain why?

Objects you experimented with:

1.\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

2.\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

3.\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

The one that works best with the sensor is \(circle one\):      1        2         3   

And this is why \(explain how you came to your conclusion\):

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

---

**Did you know**

The absolute closest you can have your target against a sensor is about one centimetre.

---

Save the program: File &gt; Save Project and then type the name: "introduction to the distance sensor".

### A different exercise

Next, let's load the program you saved in the previous chapter, named "forever loop alternating the LEDs with variable", and make some changes to it. As described in the previous chapter, to load a program from your computer's disk into mBlock, click on "File"  then click on "Load Project" and browse to your saved program in the "choose file to open" window.

Once you have the program loaded, let's make some changes to it. Delete blocks and insert new ones as necessary, until you have it the way it is shown in the image below \(Image 4.21.4\). In order to delete a block, you can right-click on it and select "delete", or drag and drop it outside the programming canvas.

![](/assets/Img.4.21.4.jpg)

\[Image 4.21.4: The new version of the program\]

The new program will make the onboard LEDs blink with a frequency that corresponds to the distance of an object detected by the ultrasonic sensor.

Here's what happens: 

* the left LED turns on \(red\) while right LED is turns off, 
* and this is maintained for an amount of time that is the result of the multiplication of _distance times 0.01 seconds_. 
* Then, the left LED is turns off while the right LED is turned on \(blue\), 
* and again is maintained for an amount of time that is the result of the multiplication of _distance times 0.01 seconds_.
* The pattern repeats, since it is placed in a forever loop. 

But why multiply with 0.01? Imagine the distance of the object being, say, 30 cm. Obviously, it wouldn't be much of a blink to have the LED stay turned on for 30 seconds and therefore, we need to multiply it with some decimal value to reduce the on/off cycle duration to something more interesting.

---

#### Did you know

The "ultrasonic sensor" block returns distance readings of the sensor are in centimetres.

---

Go ahead to "Upload to Arduino" and test your program. Pick a suitable obstacle, like a book, place it before the sensor and try different distances. The closer you bring it to the mBot, the faster the LEDs blink, and the further away you take it from the mBot, the blinking rate decreases.

This was just another example of how you can get input from sensors and then manipulate that input arithmetically in order to produce a desired behaviour. We are going to work more with the ultrasonic sensor later on in this crash course. For the time being, let's move on and talk about the if and if-else control structure.

---

#### Exercise 4.21.3: Modify the program shown in image 4.21.3 so that the LEDs have the opposite behaviour: their intensity increases, instead of decreasing, as the target object is getting closer, and vice versa.

What is your new program?



Answer: 

![](/assets/2017-04-22_12-22-56.png)

---

**Question 4.21.4: What is the way of operation of the distance/proximity sensor?**

A. The transmitter emits a specific tone and the receiver picks up the _distortion_ of the tone.

B. The transmitter emits an ultrasonic sound signal and then picks up the echo.

C. The transmitter emits an ultrasonic sound signal and the receiver picks up the echo.

D. Both A and C.

_Answer: C_

---

**Question 4.21.5: What happens when you run the program shown in image 4.21.3, with the object flat against the sensor?**

A. The sensor returns an error.

B. The sensor returns an error and stops functioning.

C. The sensor can return no valid reading.

D. The sensor returns detailed readings \(for example, millimetres instead of centimetres\).

_Answer: C_

---

