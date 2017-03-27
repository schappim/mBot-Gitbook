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

 Now that you've saved it, I'm going, to go and create a new project. To demonstrate how the ultrasonic distance sensor works, I’m going to create a very simple program. I’ll start us always with the mBot program header and then I'll pick the ultrasonic distance sensor.

Now, notice that this block does not have that indentation that allows us to connect it to the mBot program header block. Blocks with rounded corners, an indication that this block is meant to return a value. In order to use this value we need to use something like a variable to store it in. This is a hint to us that we can't do much with this block unless we store the value that the sensor returns in a variable. Let’s go and pick a variable then, make a variable and I'll give it an obvious name such as Distance and hit Okay.

Now I pick the set distance block and place it against the mBot program header. You can see that it fits. What I'll do next is that I'm going to take the ultrasonic sensor block and use it to populate the text box inside this set block. Now, I'm going to get the ultrasonic sensor to take a reading against whatever object it has in front of it and then store that value inside a distance variable. Now, the next thing that I'd like to do just to show what the result of this measurement is, I'd like to visualize it somehow. To do that, again, I'm going to work with the familiar RGB LEDs.

I'm going to take the RGB LED block, the said LED on board block and connect it to the set block. What I'd like to do is to configure the intensity of each one of the RGB LED components, the red, green and blue to the value that we've stored inside the distance variable. Let's go back to data mBlocks and pick the distance variable. You can experiment with this as you please but I'll keep it simple here, and I’ll just use the same value for all three components of the RGB LED. It's going to look – oops, do that again. It's going to look like that. Need more space, there you go.

The idea here is that as the distance increases the brightness of the LED will increase as well. As the distance from the target decreases then the brightness will also decrease. There's only one problem here, I’m going to give you a few seconds to think about it. Is there a problem that you can see in the way that I have constructed this program?

\[pause 00:07:45\]

Okay, not sure if you picked it up but the problem here is that these two instructions, these two blocks will only execute once and then the execution will stop. We are only going to take one single measurement with this sensor. It's not ideal, with a sensor typically, you want to take multiple measurements because you want your robot to continue sensing its environment to sense change. If you only take one measurement, then there's not much change that you get sense with it. How would you recommend that we fix this problem? How do you recommend that we get this sensor to continuously take measurements of the distance between itself and an object in front of it?

We'll use a control structure and ideally, we'll use the forever control structure. Since this is the one that we know at this point. Let's go and put that in the middle, we’re going to move that down. Connect forever to the mBot program header and then take the block of the two bits of code and insert them inside the forever loop. Now our program is complete. Let's test it out. Let's see what it does. Upload to Arduino. Make sure that we've got a serial port connected Comp six and upload to Arduino.

I'll increase the distance between the sensor and myself. Okay, upload is complete. Let's try it out. I just need a nice clean surface to use as target. Here's the bag, will do. You can see there's nothing in front of the sensor right now, so the two LEDs are at the brightest setting. I'm putting the bag right in front of it and you can see that we've got a fluctuation now. The intensity is becoming smaller, so the LED intensity is fainter. Eventually at some point it's going to turn off completely. Because now, if you go too close though. See what happens, if you go too close, I’m now blocking the transmitter and the receiver, you can see that the intensity is at maximum. Can you figure out why that happens?

Well, the reason for this is that we now have no way for a signal that is transmitted by the transmitter to reach the receiver. If you block either one of these two, then you basically have no way of getting of getting an accurate measurement. The absolute closest you can have your target against a sensor is about maybe one centimeter in distance. Beyond that you can take a fairly accurate measurement depending on the kind of target that you use.

I'd like you to think about one more thing before we move on to the next part of this crash course on the mBot. Do you think that you can modify this sketch so that the intensity of the LEDs actually increases as your target is getting closer to the sensor instead of decreasing? Have a think about this, how can you change a program so that intensity as the distance becomes smaller intensity of the LEDs increases? Think about this problem.

