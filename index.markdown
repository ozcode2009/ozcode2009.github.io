---
layout: default
title: ozcode
---

# ozcode's website

Hi! My name is Oliver, and I write code in my free time. Here are a few projects (but first a good story):

## A good story:

So one day, I saw a YouTube Short about how you could use a flipper zero to spam people with airpods/beats/apple tv notifications on their phone. I don't have a flipper zero, but I thought this would be funny. So I decided to grab an Apollo 3, the [Sparkfun LoRa Thing Plus expLoRaBLE](https://www.sparkfun.com/sparkfun-lora-thing-plus-explorable.html) (shout out to sparkfun for being amazing and also that board has a pretty good name), and change around the flipper zero code to work on it. Long story short, it didn't work too well. 

So, I pulled out my micro:bit, and rewrote the code once more, this time to work with a library called nimBLE. (I guess everybody likes to shove BLE into the names of their stuff.) And that, surprisingly, worked AMAZINGLY. The one thing I did notice, however, was that no Airpods or Beats notifications were showing up. Just Apple TV stuff.

* "Apple TV: Would you like to connect"
* "Apple TV: Would you like to sign in"
* "Apple TV: Enter your damn password"
* "Apple TV: Calibrate your TV because apparently samsung didn't do it well enough"
* "Apple TV: You're too stupid to use the remote we provided you with as a keyboard so why don't you just use your phone that you paid way too much money for"

I brought it to band practice that same day. I pull it out, plug the battery pack in, and I kid you not in less than a minute one kid looks up and shouts "WHO BROUGHT THE FLIPPER ZERO." I couldn't keep a straight face. I showed them this and they had a look on their face like *what kind of dark magic is this*. 

Anyway I bring it to school the next day and tell my good friend: "If you don't want the annoying Apple TV notifications, turn off your bluetooth."

* In first period, not too many people were on their phones, but I did manage to elicit a few frustrated responses from those around me. "What is it with this Apple TV"
* In second period, we had a long term sub because our teacher was on maternity leave. Our sub (eternally on their phone, broke student privacy laws) was just blaming it on the teacher next door, and everyone was fed up with it at this point.
* In third period I was having the time of my life. "This goddamn apple TV" "What does this damn thing want" "Every time I pick up my phone this apple tv shows up" Suffice it to say people were more interested in their phones than the actual lesson at that point. Shout out to the one person who learned if they turned off bluetooth that fixed it.
* Fourth and fifth period nothing much happened. I shut it off after that.

I told the CS teacher who has a bunch of micro:bits that we should put them around the school with my code on them. That never came to fruition.

I tried it again a few days ago. Too bad apple patched it. More about apple vulnerabilities I've found at the bottom.


## Now you're finished the story you can check out the projects:

### Facade

Facade is my fully featured app for designing flashcards. Here's the backstory:

My history teacher makes us make flashcards for every unit we cover, and assigns an ample portion of our grade based on these flashcards. (Which by the way, I don't think any students actually use to study for the tests or for the AP. I most certainly don't.) Anyway, I was fed up with this. And I can't just use an off the shelf tool because my history teacher wants us to cross reference other terms (underline them) from that unit in the flashcards. So, the most amazing piece of flashcard design software was born, supporting the \<u>**underline**\</u> html tag. Either way the history teacher was kind of impressed and told a few admins about it with a positive connotation, so I'd call that a win. I got a 100 on the flashcards I made with the software.

![Facade in action](https://github.com/ozcode2009/Facade/blob/main/Screenshot%202025-03-31%20202305.png?raw=true)

Facade basically takes a csv file and makes flashcards out of it. That's it. Pretty simple. Here it is: [Facade](https://github.com/ozcode2009/Facade). btw its in rust

### A basic FFmpeg video player

And when I say basic, I mean it literally just opens "video.mp4." It may still be hardcoded to my documents directory. ¯\\\_(ツ)_/¯

Buuut if you want an upgraded version of this tutorial: http://dranger.com/ffmpeg/, that's basically what [this repo](https://github.com/ozcode2009/FFmpegTest) is. Just be aware that I halfassed everything.

### Arduino Artifical Horizon

This thing is COOL. Basically it reads from an IMU on the arduino and then displays it to an artificial horizon on your computer. I even made it wireless over LoRa once. Lost the code for the wireless stuff though :(. Unfortunately I don't have any screenshots. You'll just have to take my word for it that it works. https://github.com/ozcode2009/Arduino-Artificial-Horizion

## My other endeavors

I wrote an op-ed in my school's newspaper once criticizing the policy at my school for the barring of jeans in gym class. I worked on it with a few of my good friends. Read it here: https://thechompgateway.com/2028/opinion/in-defense-of-denim-the-case-for-jeans-in-pe-class/

When you're done with the article, read the comments. Hopefully you'll get a laugh at the flame war between a valedictorian and a gym teacher.

One of the friends whom I worked with the article on has his website here: https://teched.aenoble.xyz/

## Apple's Screen Time Vulnerability
This one's interesting. So back when I was in elementary school I was forced to 15min/day of this online learning platform called IXL. I found it provided no educational benefit. It was completely unrelated to what was being done in class and oftentimes it would recommend "skills" that were waaayy out of your league (giving calculus to a fifth grader) or giving math problems like 1+1 to a fifth grader. And no, it would not teach you the calculus, just test you on it. 

(I promise this whole thing is related.) So I said why don't I just write an app in java that controls your mouse to select an answer option at random (of course it only works on multiple choice questions), then clicks submit. And repeats. And that is how you do 15 minutes of IXL a day while leaving your teachers wondering how you answered 2000 questions but didn't complete 1 skill.

Anyway I noticed a slight vulnerability on Screen Time for MacOS that was not present in iOS: if you enter the wrong passcode 5 times then click "Quit Settings," it doesn't prevent you from reopening the app and trying another 5 times in rapid succession like it does on iOS. 

So I rewrote the IXL cheater program to click the necessary buttons to guess the screen time passcode. Over and over again. It took a screenshot to see if it found it or not, and I was able to use a basic binary search to figure out what the passcode was. 

Tried it the other day and Apple patched it as well.

Contact me at: mailto:ceo@deermail.xyz (Same friend whose website I linked to made that for me.)