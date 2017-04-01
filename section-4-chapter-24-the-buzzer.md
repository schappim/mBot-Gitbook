# Section 4

---

## Chapter 23: The buzzer

---

In this chapter you will learn about:

* ---

One last thing before moving to the next section. Let's see how to use one more device that comes with the mBot: the buzzer and like the name suggests, we can use the buzzer to make some noise.

The instruction block that allows us to control the buzzer is the "play tone on note ... beat ..." and it can be found in the \(dark blue\) "Robots" section. Let's drag and drop it in the program of the previous chapter, shown in image 4.22.5, right below the instruction block that sets the LEDs to red, and then add the note attribute to E4 and the beat attribute to Quarter, just to experiment, like this:

![](/assets/Img.4.23.1.jpg)

\[Image 4.23.1: Where to add the buzzer instruction block\]

This new addition will have the mBot produce a sound when the object gets too close and the LEDs are turned to red, very much like a collition alert: "Alarm! Object too close!"

Let's "Upload to Arduino" and check it.

Moving an object too close to the mBot and the ultrasonic sensor, now, should turn the LEDs to red, like before, but also produce an alarm sound, from the buzzer.



