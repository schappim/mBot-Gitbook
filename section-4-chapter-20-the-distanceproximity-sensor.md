# Section 4

---

## Chapter 21: The distance/proximity sensor

---

In this chapter you will learn:

* How to 

---

With the two LEDs blissfully blinking away forever, the next thing that we are going to handle is the proximity sensor.

### Operation of a distance/proximity sensor

The proximity sensor allows us to measure the distance between the mBot and an object in front of it. The sensor works well in a reasonable distance up to 30 or 40 centimeters. The further away you go from the object, the larger the object has to be in order for the sensor to pick up the distance correctly. You will find, for example, that a pen might be too small for the sensor to be able to recognize it and to the measure the distance from it. A larger object with a flat surface, like a book, makes a better candidate for this kind of sensor. The principle of operation is the same by which a sonar works for a submarine: there are two components:

* the **transmiter **which them emits out a bleep: an ultrasonic sound which is going to reach the object, bounce off it and then come back
* the **receiver **which listens out for those bounced signals.

Internally the sensor will calculate the amount of time that it takes for the signal to travel to the obstacle and then to come back. From that information, it will produce out the distance in centimeters or inches, or a measuring unit which you can control.

### Programming the sensor

Let's create a new project in order to see how the ultrasonic distance sensor works: File &gt; New

As always, we start by placing the mBot program header on the canvas. Next, we drag and drop a "ultrasonic sensor ... distance" on the canvas. We will notice that this block does not have the indentation that allows it to connect to the mBot program header block.

Blocks with rounded corners, like this one, are meant to return a value. One way to use such a block is to place it within a "set variable" block, assigning the returned value to some variable.

Let's create, therefore, a new variable: Data&Blocks &gt; Make Variable

and give it the name "distance".

Next step, we drag "set distance to ..." and attach it below the header bock. And now we can move the "ultrasonic sensor ... distance" block and make it the second attribute of "set distance to ..." like shown in the image below:

![](/assets/Img.4.21.1.jpg)

\[Image 4.21.1: Assigning the ultrasonic sensor reading to variable "distance"\]

Next, we add a "set led on board ..." block, attach it to the program and place variable "distance" in all the three attribute places:

![](/assets/Img.4.21.2.jpg)

\[Image 4.21.2: Setting the LEDs to emit a quantity of light corresponding to the distance from the object\]

Τhe problem, here, is that these two instruction blocks will only execute once and then the program will stop, meaning we are going to take just one single measurement with the sensor, which is not ideal. With a sensor, typically, you want to take multiple measurements because you want your robot to continue sensing change in the environment. In order do have these two instructions execute repeatively we need to place them within a loop. So, let's add a forever loop, and arrange the blocks, by moving them around, to achieve the order shown here below:

![](/assets/Img.4.21.3.jpg)

\[Image 4.21.3: The final program\]

**Note**: The colour of the blocks can direct you as to the category where you can find each block.

The idea here is that as the distance from the object increases, the brightness of the LEDs will decrease. As the distance from the object decreases, the brightness will increase acordingly. Now that our program is complete and we can test it out and all that in practice.

We make sure that we've got a COM port connected and then "Upload to Arduino".

We place some object in front of the sensor, like a book, and then slowly move it closer to the sensor and back again. We notice that the intensity of the LEDs grows stronger or fainter, depending on the distance between the object and the sensor.

When there is no object before the mBot, or when the object is too close to the sensor, we will notice that the LEDs will be at the brightest setting. The reason for this is that in both cases there can be no reading. The signal either doesn't return or, when we are too close, there is just not enought space for the signal to travel from the transmiter to the object and back to the receiver.

**Note**: The absolute closest you can have your target against a sensor is about one centimeter.

### Exercises

1.Modify the program so that the LEDs have the oposite behaviour: their intensity increases, instead of decreasing, as the target object is getting closer, and vice versa.

### Questions

1.What is the way of operation of the distance/proximity sensor?

A. The transmiter emits a specific tone and the receiver picks up the distortion of the tone.

**B. The transmiter emits a ultrasonic sound signal and then picks up the echo.**

C. The transmiter emits a ultrasonic sound signal and the receiver picks up the echo.

D. Both A and C.

2.What happens when we run the program shown in image 4.21.3, but then with the target object leaned against the distance/proximity sensor?

A. The sensor returns an error.

B. The sensor returns and error and stops functioning. 

C. The sensor can return no valid reading.

D. The sensor returns detailed readings \(for example, milimetres instead of centimetres\).

