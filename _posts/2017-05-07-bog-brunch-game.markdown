---
layout: post
title: "Game: Bog Brunch"
categories: bog brunch game videogame webgl pixi nodejs express
main-image: /assets/bog-brunch/pixi-page.png
---

![UMSATS TSAT1]({{ site.url }}{{ page.main-image }}){:width="450px"}

**Find the live game [here](https://aqueous-refuge-74804.herokuapp.com). Find the project on GitHub [here](https://github.com/DotFreelance/floatplane). Find the documentation [here](https://github.com/DotFreelance/floatplane/wiki).**

This project is meant to be a test of my skill. My goal: Within a week and 2 days, create a game that uses a Node.js server as the backend.

**Froggly**  
What I decided upon was a small, asteroids-inspired frog game where you eat bugs to earn points and avoid wasps. To satisfy the requirements, I decided I would implement a high-score system using Node and MongoDB or CassandraDB.

_**and so it began...**_  
I received the email with details of the challenge on Friday. Throughout this project I will be posting updates to this blog post detailing the process. I hope to help others understand what sort of things I encounter from day to day and how I tackle a project like this.

### Saturday, May 6

I've chosen my technology stack, setup the `Node.js + Express` webpage and built a small
prototype using the `PIXI.js WebGL` framework.

**The Prototype**  
![Bog Brunch Prototype]({{ site.url }}/assets/bog-brunch/prototype-sample.png){:width="450px"}

Right now the prototype is simple. It allows you to move around the frog in any direction using the arrow keys, and the frog turns to face that direction. This was built before any documentation was created as a proof of concept (to myself.)

I had spent some time playing with different WebGL technology, considering:
1. `Raw WebGL` -- I have a background in Graphics, so it isn't out of the question. However, I knew this project needed to be built quickly, so I looked for frameworks.  

1. `Three.js` -- While an excellent and popular framework for building 3D games, the toolset was a bit more involved than what I needed. I had considered using [Unity]({{ site.url }}{% post_url 2017-05-01-spider-eyes %}) again at this point, but thought that it would be too "involved" for what I needed to do.  

1. But finally, `PIXI.js` won me over! This is a framework that bases itself entirely in 2D sprite games, so it seemed the obvious choice as that's exactly what I was creating.  

### Sunday, May 7

Today I have the project public in a git repository, and I've completed several of the intention documents including a [project board](https://github.com/DotFreelance/floatplane/projects/1), an [initial design document](https://github.com/DotFreelance/floatplane/wiki/Initial-Design-Plan), and an [architectural layout](https://github.com/DotFreelance/floatplane/wiki/Architecture).

**The Project Board**  
![Bog Brunch Project Board]({{ site.url }}/assets/bog-brunch/prototype-project-board.png){:width="450px"}

***
**The Balancing Act - An Excerpt About Me**  
_You can skip this bit if you only want to read about the project itself._  

Some of the hats that we have to wear as developers are as an architect and as an archivist. It's our job to not only develop software, but to do the unsavory parts -- the parts that most developers consider unsavory, anyway -- to create a plan and document it.

An influencing factor in my fervor to create initial documentation comes from my time at Electronic Arts, Inc. As a larger company, the process that one goes through is a bit more bureaucratic than you might find at a smaller startup.

And therein lies the _balancing act._ Despite my process bent, I understand that sometimes process can be too much. I like to use the term bureaucratic because it sums up how developers feel about the process. I understand that.

For me, I need at least some level of layout before I can really work on a project. I keep a notebook on hand at all times to sketch or take notes, or sometimes I just use textEdit on my Mac (or notepad on Windows) to organize my thoughts.

When I first started applying to places for my Computer Science co-op terms, I would frequently be asked what my _weakness_ was. This is one of those questions you think most people answer with _"perfectionist"_ but I chose to answer with a bit more insight into who I am, and to further provide what I thought was a reasonable method to improve upon that weakness.

For me, it was managing a project. Bringing it from idea to reality. I was poor at this. I had finished projects before, but it had always seemed so haphazard, and I never really knew if the project was done-done.

After several co-op terms and software engineering classes, I've gone out of my way to build up a system, a process that works for me. I am, of course, continually improving this process.

Part of that improvement is trimming the excess to make sure that I maintain that delicate balance between useful documentation and bureaucracy.  

***  
<br>

It is now 11:00pm on Sunday night, and I feel I have a good start on the project. I have a better idea what it will take to complete the tasks, and have them organized into a priority that makes sense. It's only a matter of time before the game has all of the elements to meet the [Minimum Viable Product](https://github.com/DotFreelance/floatplane/milestone/1).

Goodnight.

### Monday, May 8

PIXI is a pretty complete solution. It's designed specifically for what I'm attempting to do, so it's no surprise that as I face a new challenge, PIXI has the answer.

The hurdle, though, is figuring out the documentation that's available. [This documentation](https://github.com/kittykatattack/learningPixi) is incredible, but there are small gotchas, technical issues and some editorial errors.

**Hit Detection**  
Today, my task was to tackle the challenge of hit detection. Thankfully PIXI -- or more specifically _kittykatattack_ -- was prepared to help. A custom function written for rectangle hit detection right in the tutorial, and with a little modification, worked well for what I needed. Originally the function did not account for one rectangle belonging to an object that was not in the global space, thus the modification.

The hit detection for player attack is done on the tip of the tongue and the insects. This allows me to create a _projectile_ style system, and stop the tongue animation once a hit is detected.

![Bog Brunch Class Code Sample]({{ site.url }}/assets/bog-brunch/class-code-sample.png){:width="650px"}

**Points system**  
Following that, it was a simple matter of creating a `ScoreKeeper` class and submitting the score change. Each Insect sub-class maintains its own point value, so we simply tally it.

![Bog Brunch Frog]({{ site.url }}/assets/bog-brunch/new-player-sprite.png){:width="150px"}

**Fancy New Sprites!**  
So I did not expect this, but I received help with sprite generation. I now have wonderfully stylized and interesting looking sprites! I also have background static sprites! This helps me complete a lot more of the post-MVP tasks than I had expected to be able to complete within the time limit.

With the character animated, the sprites created and basic hit detection working, it's now a matter of getting the different types of insects spawning onto the board.

### Tuesday, May 9

Not much more work done today, just tidying and refactoring. It's good for the codebase and my sanity, though.

I always try to maintain a certain modularity. I try to, and pretty strictly do follow the single source of truth idea. I don't like the thought of tracking state over multiple classes, methods, etc. If something needs to be mutated, do it in one place only and always call that part of the interface.

An example of this includes the `InsectSpawner`. It tracks how many insects are on the screen, and how many are allowed to be. Having the insect value modified by the `spawn(insect)` method only means there's much less a chance of a numerical error and thus a runtime issue.

### Wednesday, May 10

Today was the day where the final major piece was completed. Or almost completed. The insects are spawning with the `InsectSpawner` and I have a `Timer` class that handles running the game timer on screen and handles events that I can pass in via an `addEvent()` interface.

![Timer Update Method]({{ site.url }}/assets/bog-brunch/game-timer-update.png){:width="550px"}

The `InsectSpawner` uses a manually created array of difficulty stages that increase the number of enemies on screen and decrease the number of food insects on screen.

Having built the event handling logic in the `Timer` class helped a lot to progress this application further.

A real goddamn **BEAR** was the `setInterval()` method in JavaScript. The issue is that it doesn't maintain the correct `this` context, which means I wouldn't be able to properly refer to the object that spawned it. In order to get around this, I used a piece of code from the MDN, the most trusted source of documentation for the web. [The "this problem"](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setInterval#The_this_problem) details the context issue and the solution I used.

Other issues I faced included me being super tired and not doing basic math properly. Ugh.

### Thursday, May 11

Today I managed to finish the `InsectSpawner` and we now have a working game. There are difficulty stages, a score and a timer. The game has a start screen and an end screen. The core of the game is complete, so it's ready to be deployed to be tested by players.

![The Core Game Complete]({{ site.url }}/assets/bog-brunch/core-game-complete.png){:width="550px"}

I plan to use **Heroku** to deploy the application. I've tagged a beta stage on git as `v0.4.0-beta` (check out [semver.org](http://www.semver.org) for more information about tagging convention) and plan to deploy the beta tonight. Hopefully I can convince a few people to play and see what happens.

If I have time, I would like to create a proper testing regime for the game as well. It looks like I may. For now, the beta will have to do and will help ensure this game is properly cross compatible.
