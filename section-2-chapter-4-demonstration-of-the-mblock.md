# Section 2

---

## Chapter 4: Demonstration of the mBlock

---

In this chapter you will learn about:

* How to control the mBot using mBlock on a tablet

---

If you have children in your family or if you’re a teacher using this information to teach your class, then mBlcok is the ideal application for kids to get started with.

Start the application and it should be able to quickly detect a nearby mBot.

**Remember**: if the Bluetooth LED on the mBot is solid blue, that means that the mBot is already connected to a previous application. Switch it off and on again to reset the connection.

You will found out that this application is given in the form of a game organized in stages that you can go through, and as you follow the instructions correctly finish each stage successfully, you earn points and rewards.

![](/assets/Img.2.4.1.jpg)

\[Image 2.4.1: The game stages\]

Tapping on the first one will get you in and there you should see Mr. Panda. Just tap anywhere on the screen to get Mr. Panda to go on with his instructions.

![](/assets/Img.2.4.2.jpg)

\[Image 2.4.2: Mr. Panda\]

After Mr. Panda's welcoming you should see the first task: Click "Play" to view mBot movements.

Tapping on "Play", on bottom right of the screen, will get the mBot to produce some actions, like buzzing and getting the motors to move a little.

Next we are going to be instructed to actually move an instruction block and place it under the other. The instructions are supplied by some explanatory animation and even a child can understand what is expected.

![](/assets/Img.2.4.3.jpg)

\[Image 2.4.3: Moving one block under another\]

Once the two blocks fit like jigsaw pieces, tap on "Play" to see them get executed. They should get the mBot to move forward for one second at a particular speed.

When done, click on "Forward" \(the orange button next to "Play"\) to get to the next task. This time we are asked to combine blocks to make the mBot first to go forwards and then to go backwards. All the blocks are already on the canvas, so you just need to drag the one that is out of place and lock it under the other two. When done, click on "Play" to see the mBot do as programmed. Just remember to make some space for it to move.

~~**{up to here by Dimitris}**~~

Let’s go next. You get the idea, this is an easy way for a person to easily learn how each of these blocks work in the format of a game. I’m going to leave for this for you to explore further and finish with this lecture. I just want to recap a couple of things.

These three applications; Makeblock, mBlockly and mBlock are great applications to get started with. They’re not very efficient because the programs that you write are using these applications to not execute directly on to the mBot. The programs execute on you iPad and then the iPad remotely controls the mBot, and the penalty here is efficiency.

If your mBot needs to make quick decisions that involve perhaps taking readings from the sensors and then changing the speed of rotation of the motors to change direction, and if this needs to happen very quickly in order, for example, to not leave the line that the robot is following, then this is not going to be possible with one of those applications. It’s just they’re just too slow to be able to do something like that. But for many other things, these three applications are an excellent way to get started.

Having said all that, in the next section and in the remainder of this course, I will be showing you how to use the mBlock application which allows to control your mBot on your Windows or Macintosh computer. This works a lot like the Arduino, so the process there is that you write your program using the Scratch language and then that program is translated to native Arduino C code without you actually having to do anything, and then it gets uploaded on to your mBot.

What eventually you get on the mBot is Arduino code that runs at maximum speed so that you can control your mBot very efficiently, can get it to do things like that, follow a live that losing its way.

Let’s move on to the next lecture and check that out.

