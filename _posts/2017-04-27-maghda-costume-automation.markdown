---
layout: post
title: "Maghda Costume Automation"
date:   2017-04-27 12:07:00 -0600
categories: maghda costume comiccon blizzcon automation robotics
main-image: /assets/maghda.jpg
---

![Jekyll Logo]({{ site.url }}{{ page.main-image }}){:width="350px"}

Building elaborate costumes for major events like San-Diego Comic Con or Blizzcon means attention to detail.

When putting together this Maghda costume, my friend and his wife **[pictured above]** needed someone to program the Arduino to make those wings flap on an interval. We also needed to setup a system that allowed her to use a button, wired into her glove, that would let her temporarily interrupt the scheduled flapping for a manual flapping, then return to the schedule.

The code was easy enough, the real challenge was the physical unit.

Servos were not enough. While easy to wire, the torque required to lift the aluminum chassis of the wings exceeded the puny servo strength.

The solution? Cheap, $3.00 power screw drivers. The torque from the gearing system was more than enough.

But ah... a new problem. The servos worked well on the 3.3v from the Arduino, but the screw drivers had a much higher 12v requirement. The final solution was to setup a 12v circuit activated by relays, controlled by the 3.3v circuit from the Arduino. It worked perfectly.

Now, if you search for Maghda in Google Images, the costume is among the top results.
