---
layout: post
title: "Touch Paint Wall"
categories: hardware
main-image: /assets/thinkingbox/touch-paint-page.jpg
---

![PAINT WALL]({{ site.url }}{{ page.main-image }}){:width="450px"}

## Summary

This was an internal project for Thinkingbox. The concept was a touchable painted mural that played music. A backing track played continuously, while the other tracks, also continuously playing, were muted and would fade in only when a region of the paint wall was touched. The paint wall would sleep after a period, awoken by a touch. It was automated to start when plugged in.

#### Construction

I used a Raspberry Pi 3 B+ to handle running the program that would translate touches into music. The wall itself was built and painted by me, using plywood, two-by-fours, spray paint, and a stencil that was printed by [East Van Vinyl](http://eastvanvinyl.com) (who printed this design very quickly for us, and it worked really well.) The touch paint was a conductive paint  purchased from BareConductive. We also purchased a BareConductive - RPi interface shield that attaches to the RPi GPIO.

#### Software

The software was written in Python. It was designed on top of PyGame to handle sounds on multiple channels, with a backing track that always played. As you touched, the other tracks would be brought up to full volume to be played over top of the backing track.

#### What It Took

This project required me to use a wide variety of skills, including handy skills for building the structure of the hanging mural, hanging the mural itself, painting, soldering, and programming. It also required a little bit of OS configuration to get the program to run on startup.

#### Learnings

1. BareConductive paint does not dry quickly, and smudges even after curing.
1. Acrylic paint does not work over BareConductive paint.
1. Spray paint is not as easy to work with as one would initially assume, but does apply nicely overtop of the BareConductive paint.
1. After the 48-hour setting period BareConductive paint conducts touch _very_ well.

#### _More to come!_