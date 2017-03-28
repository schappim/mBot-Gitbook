# Section 4

---

## Chapter 22: More with the distance/proximity sensor

---

In this chapter you will learn:

* 1

---

The next thing that I'd like to do now is to use our knowledge of the way that the ultrasonic sensor works to control the blinking rate of the two LEDs in the program that we created earlier. Let me save this progress so that we don't lose it, before I load the previous program. This is going to be-- let's make it seven. This is introduction to the distance sensor and you load the sixth program there forever loop alternating LEDs with variable. What I like to do is to get the sensor to take continuous readings of the distance between itself and a target, and then use those readings to change the frequency of the LED switching.

Let's think about how to implement this change. At the beginning of the program we are setting the variable LED on time to a fixed value, of course we would like to change that this value will now not be fixed, it will depend on the distance that the sensor sensors between itself and a target. I'm going to have to remove this from up here. the other thing that will have to do is to take continuous reading. Obviously whatever we do next will have to happen inside the forever loop. We need to take multiple readings in that case, as the first iteration of this example, I recommend that we remove the variable completely and then we use a reading from the sensor to populate the weight block.

I'm going to take the ultrasonic sensor and connect it directly into the weight seconds block. Just noticed there's something that I didn't mention earlier that the ultrasonic sensor can be connected to any one of the four ports that are available on the inboard. Right now I've got it connected to port number three. In your ultrasonic sensor block, you also need to make sure that you've selected port three. This looks like a reasonable first iteration, let's try it out. I'm going to remove these three blocks so they don't interfere with our program, and upload the program to the Arduino.

Let's try with a target now, I'm going to tilt the M Bot like this where we can see it, because there's nothing in front of the sensors, the amount of time that the red LED will stay on is quite large, it could be maybe even up to a minute because there's nothing for about a meter in front of the sensor right now. Let's put the sensor closer, I'm going to have to wait for that amount of time to elapse. What I'll do instead is to hit the reset button in order to re-execute the program. Reset is up here, let's press it. It simply takes too long, not a very good first attempt.

let's think about this, the ultrasonic sensor reports the distance in front of it in centimeters. even a distance like this would be about 10 centimeters, it would indicate a blinking rate of about 10 seconds for each color, that's a bit too long to wait. Let's use an operator, perhaps I multiply it to make this much smaller, You could use multiplier or division as well. What I would like to do is it take this delay from the sensor and multiply it by something like 0.1. I'm going to try out different values but this I multiply a 0.1. If the distance between the sensor and the target in front of it is say 10 centimeters, then multiplying it by 0.1 would result in a one-second frequency.

I'll do the same thing with the other weight block, that and that will be 0.1. All right, let's put the back and let's upload the sketch and see what happens next, just so it become six; Here's my target, now. I still think that the frequency is too high. let's go one order of magnitude smaller and change the multiplier to zero points that are one and upload again. This is the third iteration. All right, that's better, I can see that as a target goes closer to the inboard sensors, the LEDs are blinking at a faster rate and as it moves further away, the rate decreases.

This is just an example of how you can get input from sensors and then manipulate that input arithmetically in order to produce a desired resolved. We're going to work more with the ultrasonic sensor later on in this crash course. Okay, this is good, let's move on to the next part of the crash course where I'd like to talk a little bit about control structures and especially the if and the if--else control structure



