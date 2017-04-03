# Section 5

---

## Chapter 29: Implementing a U-turn a the end of the line

---

In this chapter you will learn about:

* How to make the mBot turn around when it reaches the end of the line

---

We are now getting closer to having the mBot deal with the end of line problem.

We would like to get it to turn around enough so that it can re-establish contact with the line and then continue moving in the opposite direction.

There are multiple ways to achieve the same result, programmatically.

![](/assets/Img.5.29.1.jpg)

\[Image 5.29.1: The modification to the program\]





The only modification that we need to make here is at the part of the program where we have detected that we've hit an obstacle and we want to deal with that situation there. I propose that we take a run block. We get the robot for example turn right. I want to try out number. Let's make it 255. Again I'm not sure if that number is correct. It's just a number that I've picked as a first attempt to solve this problem. I'm going to try it out on my track on the floor to see if it actually solves the problem here. That's all the risk to it. I think we can now try this and see if it works on the track.

Going to connect the mBot to my Arduino, turn it upside down. Actually probably don't have to do that because I make sure that there is any obstacle in front of it so that it doesn't take off. The mBot will be stopped as long as there is something in front of it within 10 centimeters. I can go ahead and upload the program to the Arduino. \[silence 00:02:28\] \[robot sound\]

What happens now-- made a mistake actually. Actually not a mistake but I've got a redundancy here. I'm going to do this upside down. From now I'm going to show you what I've done. See how should turn it off actually. See how here when the distance to the obstacle is less than 10 centimeters. I'm both telling the robot to run forward. It speed zero which is my previous attempt to get the robot stop. I'm also telling it to turn right at this particular speed. Obviously can't have both. One of the other should be enough because otherwise one the second block cancels the first block. The first block is not really needed. Going to get out of it and just take the right turn only and put that there and just delete the redundant previous code. I'm going to upload this code again and then go test it on the truck on the floor.

Let's go try this out. Back on the track and I will turn the mBot on and let it loose. First curve and second band. So far so good. You see the turn was executed but it's just not enough. I've done the turn I set the turn to 255 but it seems like it needs a little bit more than that to do a complete 180 degree turn. Let's go back and fix that and return then. I would like to keep the turn at still the same speed 255 but now I would like to add a little delay in here like to do that say for half a second. Give it a little bit more time to continue with a longer turn. Perhaps that will be long enough to allow it to turn by 180 degree sent to continue. Turned on and upload the new version of the sketch. Upload complete. It's going to try it out. Back in the truck and turn it on and off the goose. That went to look better didn't it. Half a second turn at 255 speed was just enough to get it really quickly back on track and off to the other direction. There you go. Now there's one last thing that I would like to do. Actually there's a couple of things but function in terms of functionality that's one more thing I would like to do. The mBot has a button here. It's right here. I'd like to use that button as in on of toggle. Likely be able to turn the robot on. The robot would not start running its motors. It will just wait for me to press on the button and that will be the trigger for the robot to start moving. When I've had enough playing around with the robot I can press the button again to stop it without having to reach for the on off switch. Want to use the button as the actual on off switch. Let's go try that out  
.

