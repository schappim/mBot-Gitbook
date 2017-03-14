# Section 1

---

## Chapter 2: Assembly: mCore tour and bluetooth module

---

In this chapter, you will learn about:

* 1
* 2
* 3

---

Now put the chassis of the mbod aside and work with the makeBlock, the microcontroller module. Remove the protective film as there is no need for this anymore. The first thing to do is to actually gently open up the casing by applying a little pressure on either side. It should come off easily as there is no screw holding it in place.

You might like to inspect all the parts that up this module. The integrated circuit in the middle is the ~~**Atmel® and **~~ATmega328/P microcontroller: the brains of the mbod. It’s the same microcontroller that you find on an Arduino UNO.

![](file:///C:\Users\dimit\AppData\Local\Temp\msohtmlclip1\01\clip_image002.jpg "Img.1.3.1.jpg")

\[Image 1: the microcontroller\]

Other interesting things that are on the microcontroller module are the infrared receiver and the infrared transmitter. With the infrared receiver, we are able to use the remote controller \(the one that comes with the mbod\) and get it to move in particular directions. We can also enable other functionality, programmatically created in the mbod. All made possible by the receiver. The transmitter, on the other hand, can get the mbod to transmit infrared signals like, for example, to other mbods.

![](file:///C:\Users\dimit\AppData\Local\Temp\msohtmlclip1\01\clip_image004.jpg "Img.1.3.2.jpg")

\[Image 2: The infrared receiver and transmiter\]

There is a buzzer, so that the input can make noises. There are two RGB-color LEDs, which can create any kind of color. In between them there is a light sensor which is used by the mbod in order to figure out whether it is day or night, whether a light is turned on or off, or simply put, whether there is light or darkness.

![](/assets/Img.1.3.3)

\[Image 3: Buzzer, LEDs and light sensor\]

**{up to here by Dimitri}**

I've got a button here so I can get my input to react to the button being pressed, it can make a noise, for example, it can start its motor, it's just a general purpose button, it's not a reset button, like this one here. There's a reset button here. If you press that, you reset the execution of the program on the mbod and basically you reset the program.

There's a reset button here if you press that, you reset the execution of the program on the mbod and basically you reset the program. Other components, of course, are the connectors. These connectors that are color coded and numbered one, two, three, and four, are the connectors where you plug in the various senses, for example, your range finder or the light follower sensor, will connect to any one of those sockets. Then on this side here, I've got connectors that are specially designed to be used with the motors, with DC motors and here is where I plug my DC motors. I've got an on-off switch, I've got the battery connectors here.

This is the USB connector that goes to my computer, which is exactly the same connector that you find on an Arduino UNO. And finally, I've got the connector for the communications module. The mbod operates with two different modules, one is just the radio frequency module and the other one is a Bluetooth module. In our case, we'll be using the Bluetooth module which is this one here. So I plug this module, very easy to connect and just align it, and plug it in and you've got it connected.

One little design issue that I found is that you can actually plug it in the other way around like this \[laughs\], and it actually aligns. It will connect but of course is not going to work because it's plugged in the wrong way. I've seen this happening in large groups of people where mistakenly somebody will just plug the module in like this, then they will cover up to put the cover back on, continue with the assembly of the mbod, and then half an hour later, the thing isn't working, it's not connecting to your computer and that's because the module was plugged in the wrong way. So be very careful here.

Notice that we've got the antenna design printed on the PCB of the module which is very noticeable and then you can see that on the mbod controller board as well, you've got etched on the control board like a shape that looks also like an antenna. That's a hint that you can give your students that you can make sure that the Bluetooth module is probably connected by aligning the antenna on the module itself with the etched, the printed shape of an antenna on the mbod controller board, and of course the pins will also match precisely.

Okay. That is done now. I'm going to put the cover back on, apply a little bit of pressure so that the clips connect and this is good.

