# Section 4

---

## Chapter 23: The buzzer

---

In this chapter you will learn about:

* How to program the buzzer to make a sound

---

**This chapter contains hands-on activities.**

You will need your mBot, and a fresh set of batteries installed.

You will need the mBlock software installed on your computer.

In this chapter you will learn about the buzzer, and how to control it in your mBot programs

---

The buzzer, like the RGB LEDs, is an integrated actuator in the mCore controller. You can use the buzzer to make your mBot create musical tones.

The instruction block by which you can control the buzzer is marked "play tone on note" and you can find it in the "Robots" section.

Find the "play tone on note" and drag and drop it in the program of the previous chapter, like you can see in image 4.23.1, right below the instruction block that sets the LEDs to red.

This block needs two parameters: the first parameter is the note, and the second is the duration. Experiment with these parameters in your program. Set the first one to E4 and the second one to "Quarter" \(or, really, to anything else you like\), just to experiment, as you can see in Image 4.23.1.

![](/assets/Img.4.23.1.jpg)

\[Image 4.23.1: Where to add the buzzer instruction block\]

This new addition will have the mBot produce a sound only when the object gets too close and the LEDs are turned to red, very much like a collision alert: "Alarm! Object too close!"

---

**Did you know**

Letters from A to G represent the different music notes. The numbers you see next to them represent the "octave", meaning whether the note is going to be in a higher or in a lower tone.

To learn more about musical notes, please read the relevant article on Wikipedia \([https://en.wikipedia.org/wiki/Category:Musical\_notes\](https://en.wikipedia.org/wiki/Category:Musical_notes%29\).

---

Upload the program to your mBot.

Moving an object too close to the mBot and the ultrasonic sensor, now, should turn the LEDs to red, as before, but also produce an alarm sound, from the buzzer.

---

**Question 4.23.1: What does the buzzer on the mBot do?**

A. It produces some hiss noise.

B. It produces one fixed alarm note.

C. It produces random beeping.

D. It produces a tone that you can control programmatically.

_Answer: D_

---

**Question 4.23.2: Adjust the program from Image 4.23.1 so that a different tone is played depending on the distance of the object from the sensor. Choose your own tones, or use C2 for detected distances larger than 30 cm, C3 for distances between 20 cm and 30 cm, and C4 for distances less than 20 cm.**

Answer: 



