# Section 2

---

## Chapter 11: Recapping

---

The three applications handled:

* Makeblock
* mBlockly
* mBlock

are great to get started with. They’re not very efficient because the programs that you write don't execute directly on to the mBot but rather on the tablet which remotely controls the mBot, and the penalty therefore is efficiency.

If your mBot needs to make quick decisions like taking readings from the sensors and then changing the speed of rotation of the motors to change direction, and if this needs to happen very quickly in order, for example, to not leave the line that the robot is following, then this is not going to be possible with one of those applications: they are just too slow for something like that.

Having said that, in the next section, and in the remainder of this course, we are going to see how we can use the mBlock application which allows us to control the mBot on a Windows or on a Macintosh computer. The process is that we write a program using the Scratch language and then that program is translated to native "Arduino C" code, which is member of the C-family programming languages, without actually having to do anything, and then it gets uploaded on to the mBot.

By executing the Arduino C code locally, we can have the mBot run at maximum speed, being able to perform tasks that require a great amount of efficiently, like following a line.

