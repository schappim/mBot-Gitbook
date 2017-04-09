# Section 4

---

## Chapter 23: The buzzer

---

In this chapter you will learn about:

* How to program the buzzer to make a sound

---

One last thing before moving to the next section. Let's see how to use one more device that comes with the mBot: the buzzer and as the name suggests, we can use the buzzer to make some noise.

The instruction block that allows us to control the buzzer is the "play tone on note \[C4\] beat \[Half\]" and it can be found in the \(dark blue\) "Robots" section. Let's drag and drop it in the program of the previous chapter, like shown in image 4.22.5, right below the instruction block that sets the LEDs to red, and then let's set the note attribute to something else, say E4, and the beat attribute to Quarter, just to experiment, like this:

![](/assets/Img.4.23.1.jpg)

\[Image 4.23.1: Where to add the buzzer instruction block\]

This new addition will have the mBot produce a sound only when the object gets too close and the LEDs are turned to red, very much like a collision alert: "Alarm! Object too close!"

**Note**: Letters from A to G represent the different music notes. Numbers you might see next to them represent the "octave", meaning whether the note is going to be in a higher or in a lower tone.

Let's "Upload to Arduino" and check it.

Moving an object too close to the mBot and the ultrasonic sensor, now, should turn the LEDs to red, as before, but also produce an alarm sound, from the buzzer.

### Questions

Question 4.23.1: What does the buzzer do?

A. It produces some hiss noise.

B. It produces one fixed alarm note.

C. It produces random beeping.

D. It produces a settable note.

