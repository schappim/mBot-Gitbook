# Section 1

---

## Chapter 3: Assembly: mCore tour and bluetooth module

---

In this chapter, you will learn about:

* 1
* 2
* 3

---

Now put the chassis of the mBot aside and work with the mCore, the microcontroller module. Remove the protective film from the bottom of the mBlock as there is no need for it anymore. The first thing to do is to gently open up the case by prying open that two sides. It should come off easily as there is no screw holding it in place.

You might like to inspect all the parts that make up this module. Let's make a list:

1. The integrated circuit in the middle is the ATmega328/P microcontroller. this is the the brain of the mBot. It’s the same microcontroller that you find on an Arduino UNO.
2. The infrared receiver and the infrared transmitter. With the infrared receiver, we are able to use the remote controller \(the one that comes with the mBot\) and get it to move in particular directions. We can program the mBot so that it performs a particular behaviour when a button of the remote controller is pressed. For example, we can program key "0" to play a tone, and button "1" to make the mBot spin.With the transmitter, on the other hand, we can get the mBot to transmit infrared signals to other mBots.
3. There is a buzzer, so that the input can make noises.
4. There are two RGB-color LEDs, which can create any kind of color. In between them there is a light sensor which is used by the mBod in order to figure out whether it is day or night, whether a light is turned on or off, or simply put, whether there is light or darkness.
5. There's a general purpose button that can be used for different reactions like making a noise, starting the motor etc.
6. There's a reset button that resets the the program on the mBod.
7. There are four number connectors \(one, two, three, and four\) where you plug in the various sensors. The range finder or the light follower sensor, for example, will connect to any one of those sockets.
8. On the side, there are connectors where we plug the DC motors.
9. There's an on-off switch.
10. There battery connectors.
11. There is a USB connector that goes to the computer, which is exactly the same connector that you find on an Arduino UNO. 
12. And finally, there's a connector for the communications module. The mBod operates with two different modules, one is just the radio frequency module and the other one is a Bluetooth module. In our case, we'll be using the Bluetooth module which is very easy to connect: Just align it, plug it in and you've got it connected.

**Be aware!** One little design issue that I found is that you can actually plug it in the other way around! It will connect but of course it is not going to work because it's plugged in the wrong way. I've seen this happening in large groups of people where mistakenly somebody will just plug the module, then put the cover back on, continue with the assembly of the mBod, and then half an hour later, the thing isn't working and that's because the module was plugged in the wrong way. So be very careful here.

Notice that we've got the antenna design printed on the PCB of the module which is very noticeable and then you can see that on the mbod controller board as well, you've got etched on the control board like a shape that looks also like an antenna. That's a hint that you can give your students that you can make sure that the Bluetooth module is probably connected by aligning the antenna on the module itself with the etched, the printed shape of an antenna on the mbod controller board, and of course the pins will also match precisely.

Okay. That is done now. I'm going to put the cover back on, apply a little bit of pressure so that the clips connect and this is good.

